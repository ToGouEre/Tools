# Tools

一些自用的网页小工具,纯前端,打开即用。

托管地址:**https://togouere.github.io/Tools/toolkit.html**

## toolkit.html — 评测 JSONL → XLSX 转换器

把评测导出的 `.jsonl` 直接转成 `.xlsx`,支持两种 schema:

- **多配置评测**:每个 score config 占 `[xxx] 分数` / `[xxx] 理由` 两列,列数按文件里实际出现的 score 动态确定
- **竞技场对比**:单一 `score_config / score_value / score_comment`

提取字段:`query / baseline_answer / eval_answer / thinking / key_point`(thinking 来自 `traceOutput.final_output.content[]` 里 `type=think/thinking/reasoning` 的块)。

### 用法

1. 打开页面
2. 拖入 `.jsonl` / `.ndjson` / `.json`
3. 选模式(自动识别 / 强制多配置 / 强制竞技场)
4. 点「开始转换」→ 下载 `.xlsx`

### 实现要点

- 纯前端,零后端,打开本地文件不上传任何东西
- 使用 [SheetJS xlsx](https://sheetjs.com/) 0.18.5
- 库里 `32767 字符` 的硬限制已解除(见 `lib/xlsx.full.min.js`,注释 `/* length check removed */`);Excel 自身规格上限仍是 32767,超过后不同阅读器表现不一
- 产物始终是单个 xlsx,不打 zip,不截断,不做任何额外处理

## 结构

```
toolkit.html            主页面
lib/xlsx.full.min.js    patched 版 SheetJS(仅去除单元格长度硬校验)
```

## License

自用工具,MIT-0 / 公有领域均可,没啥特别要求。
