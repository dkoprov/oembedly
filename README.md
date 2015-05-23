# oEmbed.ly
[oEmbed.ly](http://oEmbed.ly/) provides a detailed list of oEmbed providers, allowing everyone to add and promote online services supporting [oEmbed](http://oembed.com/).

## Add oEmbed Provider

To add new oEmbed provider we need two files:

* providers/**{provider}**.png
* providers/**{provider}**.json

json example for YouTube:
```
{
	"id":          "youtube",
	"name":        "YouTube",
	"description": "YouTube is the world's most popular online video community.",
	"type":        "video",
	"url":         "https://www.youtube.com/",
	"icon":        "http://oEmbed.ly/providers/youtube.png",
	"endpoints": [
		"https://www.youtube.com/oembed/"
	],
	"regex": [
		"#(http:|https:)?//(www.)?youtu.be/.*#i",
		"#(http:|https:)?//(www.)?youtube.com/v/.*#i",
		"#(http:|https:)?//(www.)?youtube.com/embed/.*#i",
		"#(http:|https:)?//(www.)?youtube.com/gif.*#i",
		"#(http:|https:)?//(www.)?youtube.com/watch.*#i",
		"#(http:|https:)?//(www.)?youtube.com/profile.*#i",
		"#(http:|https:)?//(www.)?youtube.com/playlist.*#i"
	],
	"parameters": {
		"format": "xml|json",
		"scheme": "http|https",
		"url": ""
	}
}
```

## Allowed Parameters

Parameter     | Description                   | More Info
------------- | ----------------------------- | ---------
id            | Provider unique id.           | 
name          | Provider name.                | 
description   | Provider description.         | 
type          | Provider content type.        | Types: link, photo, video, audio, or rich.
url           | Provider site URL.            | 
icon          | Provider icon.                | Size: 256x256. Format: png
endpoints     | A list of oEmbed endpoints.   | 
regex         | A list of URL structures.     | 
parameters    | A list of allowed parameters. | 

## Approval Process

Each provider will be manually approved. Be patient.
