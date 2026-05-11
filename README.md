# Patched FFmpeg DLLs for Qt Multimedia Speex Testing

Upstream issue: https://github.com/xiaoyifang/goldendict-ng/issues/1738#issuecomment-4419566511

This repository builds FFmpeg 7.1.3 Windows shared DLLs with two upstream
Speex decoder fixes cherry-picked from FFmpeg master:

- `4a0e1cfc6f33d152e007849f6de7028d651de2af`
- `c14b837dedade432a5f95981c3b1677099015376`

The goal is to keep the FFmpeg 7.1 ABI used by Qt Multimedia
(`avcodec-61.dll`) while testing whether the patched Speex decoder fixes
GoldenDict-ng pronunciation audio.

Trigger the workflow manually from GitHub Actions. The artifact contains the
runtime DLLs to test against a portable GoldenDict-ng Windows build.
