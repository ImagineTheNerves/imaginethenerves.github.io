---
permalink: /lameapi/devicelist.json
---
{
{% for device in site.devices %}
	"{{device.codename}}": {
	"fullname": "{{device.fullname}}",
	"maintainer": "{{device.maintainer}}",
	"xdathread": "{{device.xdathread}}",
	"filename": "{{device.filename}}",
	"buildsize": "{{device.buildsize}}",
	"mirrorlink": "{{device.mirrorlink}}",
	"changelog": "{{device.changelog}}"
}{% unless forloop.last %},{% endunless %}
{% endfor %}
}