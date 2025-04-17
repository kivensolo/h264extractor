# H264提取器
Wireshark 插件，用于从 RTP 数据包中提取 H264 流，支持单 NAL 单元模式（RTP 包封装模式 0）、FU-A 和 STAP-A。此外，还支持 Opus 流的提取。

# 如何使用 H264提取器
- 将 rtp_h264_extractor.lua 复制到 Wireshark 安装目录
- 编辑 init.lua 文件，确保 "disable_lua = false" 并添加 "dofile(DATA_DIR..'rtp_h264_extractor.lua')"
- 在 Wireshark 中打开 pcap 文件时，解码为 RTP 并配置 H264 动态有效负载类型。
- 菜单 - 工具 - 从 RTP 提取 H264 流

# 如何使用 Opus 提取器
- 将 rtp_opus_extractor.lua 复制到 Wireshark 安装目录
- 编辑 init.lua 文件，确保 "disable_lua = false" 并添加 "dofile(DATA_DIR..'rtp_opus_extractor.lua')"
- 在 Wireshark 中打开 pcap 文件时，解码为 RTP。
- 菜单 - 工具 - 从 RTP 提取 Opus 流

# 学习教程
[Wireshark H264 视频解码](https://blog.networkcentric.org/wireshark-h264-video-decoding/)

# 参考文献
- [Wireshark Lua](https://wiki.wireshark.org/Lua)
- [RFC6184](https://tools.ietf.org/html/rfc6184)
- [RFC7587](https://tools.ietf.org/html/rfc7587)
- [RFC7798](https://tools.ietf.org/html/rfc7798)
