# 播放链接刷新 (PLAYURL_RELOAD)

该cmd通常不提供播放链接。

## 下发条件

服务器认为需要播放链接刷新时下发，通常是多个画质可用时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `PLAYURL_RELOAD` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| reload_option | obj | 刷新选项? |  |
| playurl | obj | 播放链接信息 |  |

`data.reload_option` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| reload_stream_name | arr | 空数组? |  |
| reload_format | arr | 空数组? |  |
| scatter | num |  |  |

`data.playurl` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cid | num | 直播间真实id |  |
| g_qn_desc | arr | 画质描述 |  |
| stream | arr | 直播流信息 |  |
| p2p_data | obj | P2P信息 |  |
| dolby_qn | null | dolby画质信息? |  |

`data.playurl.g_qn_desc` 数组:

| 索引 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| 0 | obj | 首个画质信息 |  |
| … | obj | 多个画质信息 |  |
| i | obj | 最后画质信息 |  |

`data.playurl.g_qn_desc` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| qn | num | 画质代码 |  |
| desc | str | 画质描述 |  |
| hdr_desc | str |  |  |
| attr_desc | null |  |  |
| hdr_type | num |  |  |
| media_base_desc | null 或 obj | 媒体描述 |

`data.playurl.g_qn_desc[i].media_base_desc` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| detail_desc | obj | 详细? |  |
| brief_desc | obj | 简洁? |  |

`data.playurl.g_qn_desc[i].media_base_desc.detail_desc` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| desc | str | 画质描述 |  |
| tag | arr | 画质标签 | 字符串数组，部分画质存在 |

`data.playurl.g_qn_desc[i].media_base_desc.brief_desc` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| desc | str | 画质描述 |  |
| badge | str | 画质描述 | 部分画质存在 |

`data.stream` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| protocol_name | str | 协议名称 |  |
| format | arr | 封装格式列表 |  |

`data.stream[i].format` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| format_name | str | 视频封装格式名称 |  |
| codec | arr | 编码列表 |  |
| master_url | str |  |  |

`data.stream[i].format[i].codec` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| codec_name | str | 视频编码名称 |  |
| current_qn | num | 当前画质代码? |  |
| accept_qn | arr | 允许的画质代码? | 数字数组 |
| base_url | str |  |  |
| url_info | arr |  |  |
| hdr_qn | null |  |  |
| dolby_type | num |  |  |
| attr_name | str |  |  |
| hdr_type | num |  |  |
| drm | bool |  |  |
| drm_key_systems | null |  |  |
| video_codecs | obj | 视频编码信息 | 不一定存在 |
| audio_codecs | obj | 音频编码信息 | 不一定存在 |

`data.stream[i].format[i].codec[i].video_codecs` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| base | str | 编码格式 |  |

`data.stream[i].format[i].codec[i].audio_codecs` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| base | str | 编码格式 |  |

`data.playurl.p2p_data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| p2p | bool |  |  |
| p2p_type | num |  |  |
| m_p2p | bool |  |  |
| m_servers | null |  |  |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "PLAYURL_RELOAD",
	"data": {
		"reload_option": {
			"reload_stream_name": [],
			"reload_format": [],
			"scatter": 3000
		},
		"playurl": {
			"cid": 41682,
			"g_qn_desc": [
				{
					"qn": 30000,
					"desc": "杜比",
					"hdr_desc": "",
					"attr_desc": null,
					"hdr_type": 0,
					"media_base_desc": null
				},
				{
					"qn": 20000,
					"desc": "4K",
					"hdr_desc": "",
					"attr_desc": null,
					"hdr_type": 0,
					"media_base_desc": null
				},
				{
					"qn": 10000,
					"desc": "原画",
					"hdr_desc": "",
					"attr_desc": null,
					"hdr_type": 0,
					"media_base_desc": {
						"detail_desc": {
							"desc": "1080P 原画",
							"tag": [
								"高帧率"
							]
						},
						"brief_desc": {
							"desc": "1080P",
							"badge": "原画"
						}
					}
				},
				{
					"qn": 400,
					"desc": "蓝光",
					"hdr_desc": "",
					"attr_desc": null,
					"hdr_type": 0,
					"media_base_desc": null
				},
				{
					"qn": 250,
					"desc": "超清",
					"hdr_desc": "",
					"attr_desc": null,
					"hdr_type": 0,
					"media_base_desc": {
						"detail_desc": {
							"desc": "720P 超清"
						},
						"brief_desc": {
							"desc": "720P"
						}
					}
				},
				{
					"qn": 150,
					"desc": "高清",
					"hdr_desc": "",
					"attr_desc": null,
					"hdr_type": 0,
					"media_base_desc": null
				},
				{
					"qn": 80,
					"desc": "流畅",
					"hdr_desc": "",
					"attr_desc": null,
					"hdr_type": 0,
					"media_base_desc": null
				}
			],
			"stream": [
				{
					"protocol_name": "http_stream",
					"format": [
						{
							"format_name": "flv",
							"codec": [
								{
									"codec_name": "avc",
									"current_qn": 10000,
									"accept_qn": [
										10000
									],
									"base_url": "",
									"url_info": [],
									"hdr_qn": null,
									"dolby_type": 0,
									"attr_name": "",
									"hdr_type": 0,
									"drm": false,
									"drm_key_systems": null,
									"video_codecs": {
										"base": "avc1.64002a"
									},
									"audio_codecs": {
										"base": "mp4a.40.2"
									}
								},
								{
									"codec_name": "hevc",
									"current_qn": 250,
									"accept_qn": [
										250
									],
									"base_url": "",
									"url_info": [],
									"hdr_qn": null,
									"dolby_type": 0,
									"attr_name": "",
									"hdr_type": 0,
									"drm": false,
									"drm_key_systems": null,
									"video_codecs": {
										"base": "hvc1.1.6.L120"
									},
									"audio_codecs": {
										"base": "mp4a.40.2"
									}
								}
							],
							"master_url": ""
						}
					]
				},
				{
					"protocol_name": "http_hls",
					"format": [
						{
							"format_name": "ts",
							"codec": [
								{
									"codec_name": "avc",
									"current_qn": 10000,
									"accept_qn": [
										10000
									],
									"base_url": "",
									"url_info": [],
									"hdr_qn": null,
									"dolby_type": 0,
									"attr_name": "",
									"hdr_type": 0,
									"drm": false,
									"drm_key_systems": null,
									"video_codecs": {
										"base": "avc1.64002a"
									},
									"audio_codecs": {
										"base": "mp4a.40.2"
									}
								},
								{
									"codec_name": "hevc",
									"current_qn": 250,
									"accept_qn": [
										250
									],
									"base_url": "",
									"url_info": [],
									"hdr_qn": null,
									"dolby_type": 0,
									"attr_name": "",
									"hdr_type": 0,
									"drm": false,
									"drm_key_systems": null,
									"video_codecs": {
										"base": "hvc1.1.6.L120"
									},
									"audio_codecs": {
										"base": "mp4a.40.2"
									}
								}
							],
							"master_url": ""
						},
						{
							"format_name": "fmp4",
							"codec": [
								{
									"codec_name": "avc",
									"current_qn": 10000,
									"accept_qn": [
										10000
									],
									"base_url": "",
									"url_info": [],
									"hdr_qn": null,
									"dolby_type": 0,
									"attr_name": "",
									"hdr_type": 0,
									"drm": false,
									"drm_key_systems": null,
									"video_codecs": {
										"base": "avc1.64002a"
									},
									"audio_codecs": {
										"base": "mp4a.40.2"
									}
								},
								{
									"codec_name": "hevc",
									"current_qn": 250,
									"accept_qn": [
										250
									],
									"base_url": "",
									"url_info": [],
									"hdr_qn": null,
									"dolby_type": 0,
									"attr_name": "",
									"hdr_type": 0,
									"drm": false,
									"drm_key_systems": null,
									"video_codecs": {
										"base": "hvc1.1.6.L120"
									},
									"audio_codecs": {
										"base": "mp4a.40.2"
									}
								}
							],
							"master_url": ""
						}
					]
				}
			],
			"p2p_data": {
				"p2p": false,
				"p2p_type": 0,
				"m_p2p": false,
				"m_servers": null
			},
			"dolby_qn": null
		}
	}
}
```

</details>
