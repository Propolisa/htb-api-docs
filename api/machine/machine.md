---
layout: page
title: Machine
parent: Home
nav_order: 3
---


<img src="https://app.hackthebox.eu/images/icons/ic-icons-kickass/ic-machines-dark-border.svg" style="max-width:128px;float:right;" width="128px"/>

## Machine

It's everything you wanted to know about Hack The Box machines, all in one place!

### Listing Machines
#### Active


<span class="label label-green">GET</span>
Get a list of active machines:
```js
/api/v4/machine/list
```

```json
{
	"info": [{
		"id": 227,
		"name": "Fatty",
		"os": "Linux",
		"points": 50,
		"static_points": 50,
		"release": "2020-02-08T17:00:00.000000Z",
		"user_owns_count": 1222,
		"root_owns_count": 1148,
		"authUserInUserOwns": null,
		"authUserInRootOwns": null,
		"isTodo": true,
		"stars": "4.7",
		"difficulty": 78,
		"feedbackForChart": {
			"counterCake": 45,
			"counterVeryEasy": 17,
			"counterEasy": 21,
			"counterTooEasy": 37,
			"counterMedium": 478,
			"counterBitHard": 101,
			"counterHard": 199,
			"counterTooHard": 313,
			"counterExHard": 418,
			"counterBrainFuck": 832
		},
		"feedbackForChartArr": [45, 17, 21, 37, 478, 101, 199, 313, 418, 832],
		"avatar": "\/storage\/avatars\/434a84b479e2121f8dbf2c7c56becffd.png",
		"difficultyText": "Insane",
		"playInfo": {
			"isSpawned": false,
			"isActive": null,
			"active_player_count": null,
			"expires_at": null
		},
		"free": true,
		"maker": {
			"id": 103578,
			"name": "qtc",
			"avatar": "\/storage\/avatars\/f89afe1ab159ad520ba3a63e50cd59ed.png",
			"isRespected": false
		},
		"maker2": null,
		"recommended": 1
	}, "[ other machine objects ]"]
}
```

#### Retired

<span class="label label-green">GET</span>
Get a list of retired machines:
```js
/api/v4/machine/list/retired
```

```json
{
	"info": [{
		"id": 1,
		"name": "Lame",
		"os": "Linux",
		"points": 0,
		"static_points": 20,
		"release": "2017-03-14T19:54:51.000000Z",
		"user_owns_count": 19434,
		"root_owns_count": 20863,
		"authUserInUserOwns": null,
		"authUserInRootOwns": null,
		"isTodo": false,
		"stars": "4.3",
		"difficulty": 26,
		"feedbackForChart": {
			"counterCake": 13228,
			"counterVeryEasy": 8668,
			"counterEasy": 4652,
			"counterTooEasy": 1520,
			"counterMedium": 7519,
			"counterBitHard": 262,
			"counterHard": 152,
			"counterTooHard": 111,
			"counterExHard": 50,
			"counterBrainFuck": 115
		},
		"feedbackForChartArr": [13228, 8668, 4652, 1520, 7519, 262, 152, 111, 50, 115],
		"avatar": "\/storage\/avatars\/fb2d9f98400e3c802a0d7145e125c4ff.png",
		"difficultyText": "Easy",
		"playInfo": {
			"isSpawned": true,
			"isActive": false,
			"active_player_count": null,
			"expires_at": null
		},
		"free": false,
		"maker": {
			"id": 1,
			"name": "ch4p",
			"avatar": "\/storage\/avatars\/08c255a334e10b3033ab7263e6b32422.png",
			"isRespected": false
		},
		"maker2": null,
		"recommended": 0,
		"tags": [{
			"id": 73,
			"tag_category_id": 6
		}, {
			"id": 81,
			"tag_category_id": 11
		}]
	}, "[ other machine objects ]"]
}
```

### Recommended Machines

<span class="label label-green">GET</span>
Get the latest box recommendation cards, fresh from the desk of HTB moderators:
```js
/api/v4/machine/recommended
```

```json
{
	"state": ["live", "staff_pick"],
	"card1": {
		"id": 261,
		"name": "Intense",
		"os": "Linux",
		"release": "2020-07-04T16:00:00.000000Z",
		"difficultyText": "Hard",
		"avatar": "\/storage\/avatars\/41fa976e012eb51bee13efc5419ce8ac.png",
		"feedbackForChart": {
			"counterCake": 1,
			"counterVeryEasy": 1,
			"counterEasy": 2,
			"counterTooEasy": 6,
			"counterMedium": 15,
			"counterBitHard": 17,
			"counterHard": 19,
			"counterTooHard": 11,
			"counterExHard": 7,
			"counterBrainFuck": 8
		}
	},
	"card2": {
		"id": 235,
		"name": "Cascade",
		"os": "Windows",
		"release": "2020-03-28T17:00:00.000000Z",
		"retired_date": null,
		"difficultyText": "Medium",
		"avatar": "\/storage\/avatars\/64fef851357b8de1c4834093bf3426f2.png",
		"feedbackForChart": [118, 182, 774, 1389, 2846, 1108, 865, 440, 141, 179]
	}
}
```

### Machine Vulnerability Tags
#### Enumerate machine exploit categorization tags.


<span class="label label-green">GET</span>
Get the machine exploit categorization tags:
```js
/api/v4/machine/tags/list
```

```json
{
	"info": [{
		"id": 7,
		"name": "Attack Path",
		"tags": [{
			"id": 75,
			"tag_category_id": 7,
			"name": "Web"
		}, {
			"id": 76,
			"tag_category_id": 7,
			"name": "Network"
		}, {
			"id": 77,
			"tag_category_id": 7,
			"name": "Binary Exploit"
		}, {
			"id": 91,
			"tag_category_id": 7,
			"name": "Active Directory"
		}, {
			"id": 92,
			"tag_category_id": 7,
			"name": "SMB"
		}, {
			"id": 93,
			"tag_category_id": 7,
			"name": "FTP"
		}]
	}, {
		"id": 11,
		"name": "Attack Sub",
		"tags": [{
			"id": 81,
			"tag_category_id": 11,
			"name": "Injection"
		}, {
			"id": 86,
			"tag_category_id": 11,
			"name": "CMS Exploit"
		}, {
			"id": 90,
			"tag_category_id": 11,
			"name": "Web Fuzzing"
		}, {
			"id": 94,
			"tag_category_id": 11,
			"name": "Arbitrary File Upload"
		}, {
			"id": 95,
			"tag_category_id": 11,
			"name": "LFI"
		}, {
			"id": 96,
			"tag_category_id": 11,
			"name": "RFI"
		}, {
			"id": 97,
			"tag_category_id": 11,
			"name": "Password Reuse"
		}, {
			"id": 98,
			"tag_category_id": 11,
			"name": "Outdated Software"
		}, {
			"id": 99,
			"tag_category_id": 11,
			"name": "Patch Management"
		}, {
			"id": 100,
			"tag_category_id": 11,
			"name": "SUID"
		}, {
			"id": 101,
			"tag_category_id": 11,
			"name": "SQLi"
		}, {
			"id": 102,
			"tag_category_id": 11,
			"name": "DNS Zone Transfer"
		}, {
			"id": 103,
			"tag_category_id": 11,
			"name": "Cryptography"
		}, {
			"id": 104,
			"tag_category_id": 11,
			"name": "Padding Oracle Attack"
		}, {
			"id": 105,
			"tag_category_id": 11,
			"name": "File Misconfiguration"
		}, {
			"id": 106,
			"tag_category_id": 11,
			"name": "XSS"
		}, {
			"id": 108,
			"tag_category_id": 11,
			"name": "Sandbox Escape"
		}, {
			"id": 109,
			"tag_category_id": 11,
			"name": "Port Knocking"
		}, {
			"id": 110,
			"tag_category_id": 11,
			"name": "SSRF"
		}, {
			"id": 111,
			"tag_category_id": 11,
			"name": "API Fuzzing"
		}, {
			"id": 114,
			"tag_category_id": 11,
			"name": "XXE"
		}, {
			"id": 115,
			"tag_category_id": 11,
			"name": "Log Poisoning"
		}, {
			"id": 116,
			"tag_category_id": 11,
			"name": "Deserialisation"
		}, {
			"id": 118,
			"tag_category_id": 11,
			"name": "Client side attack"
		}, {
			"id": 120,
			"tag_category_id": 11,
			"name": "Kerberoasting"
		}, {
			"id": 121,
			"tag_category_id": 11,
			"name": "CSRF"
		}, {
			"id": 122,
			"tag_category_id": 11,
			"name": "AppLocker Bypass"
		}, {
			"id": 123,
			"tag_category_id": 11,
			"name": "SSL"
		}, {
			"id": 124,
			"tag_category_id": 11,
			"name": "Account Misconfiguration"
		}, {
			"id": 125,
			"tag_category_id": 11,
			"name": "File System Forensics"
		}, {
			"id": 127,
			"tag_category_id": 11,
			"name": "Process Inspection"
		}, {
			"id": 129,
			"tag_category_id": 11,
			"name": "DLL Hijack"
		}, {
			"id": 130,
			"tag_category_id": 11,
			"name": "Environment Misconfiguration"
		}, {
			"id": 131,
			"tag_category_id": 11,
			"name": "DBMS Misconfiguration"
		}, {
			"id": 132,
			"tag_category_id": 11,
			"name": "Printer Exploit"
		}]
	}, {
		"id": 9,
		"name": "Languages",
		"tags": [{
			"id": 78,
			"tag_category_id": 9,
			"name": "PHP"
		}, {
			"id": 80,
			"tag_category_id": 9,
			"name": "Python"
		}, {
			"id": 83,
			"tag_category_id": 9,
			"name": "SQL"
		}, {
			"id": 84,
			"tag_category_id": 9,
			"name": "Bash"
		}, {
			"id": 85,
			"tag_category_id": 9,
			"name": "Powershell"
		}, {
			"id": 87,
			"tag_category_id": 9,
			"name": "Java"
		}, {
			"id": 88,
			"tag_category_id": 9,
			"name": "Ruby"
		}, {
			"id": 89,
			"tag_category_id": 9,
			"name": "Perl"
		}, {
			"id": 107,
			"tag_category_id": 9,
			"name": "JSON"
		}, {
			"id": 113,
			"tag_category_id": 9,
			"name": "C"
		}, {
			"id": 117,
			"tag_category_id": 9,
			"name": "JavaScript"
		}, {
			"id": 119,
			"tag_category_id": 9,
			"name": "VBScript"
		}, {
			"id": 126,
			"tag_category_id": 9,
			"name": "VBA"
		}]
	}]
}
```
