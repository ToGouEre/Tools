# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## User Preferences

- **不要私自保存截图**(用户明确要求,2026-04-23)
  - `browser screenshot` 会自动把 PNG 写到 `C:\Users\Administrator\.openclaw\media\browser\`
  - 用完发完必须立即 `Remove-Item` 清理
  - 能不截就不截;只在必须可视化确认时用,用完删
  - 同理对 `exec` 生成的中间文件:`_serve.js` / `_syntax_check.js` / `_test_*` 完事清

## What Goes Here

Things like:

- Camera names and locations
- SSH hosts and aliases
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## Examples

```markdown
### Cameras

- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH

- home-server → 192.168.1.100, user: admin

### TTS

- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

---

Add whatever helps you do your job. This is your cheat sheet.
