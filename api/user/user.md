---
layout: page
title: User
parent: Home
nav_order: 2
---

<img src="https://app.hackthebox.eu/images/icons/ic-icons-kickass/ic-ranks-big2.svg" style="max-width:128px;float:right;" width="128px"/>
## User

These queries should be suffixed by the user ID, (demo: `9001`)
### Profile
<span class="label label-green">GET</span>
Complete profile details for user:
```js
https://www.hackthebox.eu/api/v4/user/profile/basic/9001
```
```json
{
	"profile": {
		"id": 9001,
		"name": "L33tUser",
		"timezone": "UTC",
		"isVip": true,
		"avatar": "\/storage\/avatars\/e6baffa3faa648fabf69761ca492213a.png",
		"points": 225,
		"system_owns": 25,
		"user_owns": 26,
		"user_bloods": 3,
		"system_bloods": 4,
		"respects": 5994,
		"country_name": "Fiji",
		"country_code": "TR",
		"team": {
			"name": "PartyFunbois",
			"ranking": 1,
			"avatar": "\/storage\/teams\/8232e119d8f59aa83050a741631803d6.jpg"
		},
		"university_name": "L33t University",
		"description": "Hi I am L33t Hax0r, I like to hack box and profit",
		"github": "https://github.com/l33tb0i",
		"linkedin": "https://www.linkedin.com/in/L33tB0i/",
		"twitter": null,
		"website": null,
		"server": "EU VIP 27",
		"rank": "Guru",
		"rank_id": 4,
		"current_rank_progress": 0,
		"next_rank": "Omniscient",
		"next_rank_points": 31.331999999999997,
		"rank_ownership": "99.76",
		"rank_requirement": 45,
		"ranking": 23
	}
}
```
#### Activity

<span class="label label-green">GET</span>
Complete list of owns involving a machine (user / root), challenge, or Endgame, for a given UID:
```js
https://www.hackthebox.eu/api/v4/user/profile/activity/9001
```

```json
{
	"profile": {
		"activity": [{
			"date": "2020-07-05T12:43:33.000000Z",
			"date_diff": "1 day ago",
			"object_type": "machine",
			"type": "root",
			"id": 261,
			"name": "Intense",
			"points": 40,
			"machine_avatar": "\/storage\/avatars\/41fa976e012eb51bee13efc5419ce8ac_thumb.png"
		}, {
			"date": "2020-07-03T20:02:11.000000Z",
			"date_diff": "3 days ago",
			"object_type": "challenge",
			"type": "challenge",
			"id": 131,
			"name": "ID Exposed",
			"points": 2,
			"challenge_category": "OSINT"
		}, {
			"date": "2020-06-21T16:30:54.000000Z",
			"date_diff": "2 weeks ago",
			"object_type": "endgame",
			"type": "endgame",
			"id": 4,
			"name": "RPG",
			"points": 40,
			"flag_title": "Collapse of the empire"
		}, {
			"date": "2020-05-20T15:01:04.000000Z",
			"date_diff": "1 month ago",
			"object_type": "fortress",
			"type": "fortress",
			"id": 2,
			"name": "AKERVA",
			"points": 15,
			"flag_title": "Little Secret"
		}, ... 
		]
	}
}
```

#### Progress

<span class="label label-green">GET</span>
Machine progress for user:
```js
https://www.hackthebox.eu/api/v4/user/profile/progress/machines/os/9001
```
```json
{
	"profile": {
		"operating_systems": [{
			"name": "Linux",
			"completion_percentage": 10,
			"owned_machines": 11,
			"total_machines": 110
		   {"name": "Windows" ... },
		   {"name": "FreeBSD" ... },
		   {"name": "Solaris" ... },
		   {"name": "Other"   ... }
		]
	}
}

```

<span class="label label-green">GET</span>
Challenge progress for user:
```js
https://www.hackthebox.eu/api/v4/user/profile/progress/challenges/9001
```
```json
{
	"profile": {
		"challenge_owns": {
			"solved": 100,
			"total": 127
		},
		"challenge_categories": [{
			"name": "Reversing",
			"owned_flags": 2,
			"total_flags": 19,
			"completion_percentage": 11,
			"avg_user_solved": 0.77
		},
		{"name": "Crypto"    ... },
		{"name": "Stego"     ... },
		{"name": "Pwn"       ... },
		{"name": "Web"       ... },
		{"name": "Misc"      ... },
		{"name": "Forensics" ... },
		{"name": "Mobile"    ... },
		{"name": "OSINT"     ... },
		{"name": "Hardware"  ... },
		]
	}
}
```

`[GET]` Endgame progress for user:
```js
https://www.hackthebox.eu/api/v4/user/profile/progress/endgame/9001
```
```json
{
	"profile": {
		"endgames": [{
			"name": "P.O.O.",
			"completion_percentage": 0,
			"owned_flags": 0,
			"total_flags": 5
			},
			{"name": "Xen"   ... },
			{"name": "Hades" ... },
			{"name": "RPG"   ... }
		]
	}
}

```


`[GET]` Fortress progress for user:
```js
https://www.hackthebox.eu/api/v4/user/profile/progress/fortress/9001
```
```json
{
	"profile": {
		"fortresses": [{
			"name": "Jet",
			"avatar": "https:\/\/www.hackthebox.eu\/storage\/companies\/3.png",
			"completion_percentage": 0,
			"owned_flags": 0,
			"total_flags": 11
        },
        {   "name": "Akerva" ...  },
		]
	}
}
```

`[GET]` Pro Lab progress for user:
```js
https://www.hackthebox.eu/api/v4/user/profile/progress/prolab/9001
```
```json
{
	"profile": {
		"prolabs": [{
			"name": "RastaLabs",
			"subscribed": false,
			"completion_percentage": 0,
			"owned_flags": 14,
			"total_flags": 20,
			"total_machines": 14,
			"average_ratings": 4.87
		},
		{	"name": "Offshore"    ...	},
		{	"name": "Cybernetics" ...	}
		]
	}
}
```
#### Graph

`[GET]` Chart data for one week, daily step:
```js
https://www.hackthebox.eu/api/v4/user/profile/graph/1W/9001
```
```json
{
	"profile": {
		"graphData": {
			"user_owns": [71, 71, 71, 71, 71, 71, 71],
			"system_owns": [71, 71, 71, 71, 71, 71, 71],
			"challenge_owns": [90, 90, 90, 90, 90, 90, 91],
			"first_bloods": [0, 0, 0, 0, 0, 0, 0],
			"respects": [17, 17, 17, 17, 18, 18, 18]
		}
	}
}
```

`[GET]` Chart data for one month, weekly step:
```js
https://www.hackthebox.eu/api/v4/user/profile/graph/1Y/9001
```
```json
{
	"profile": {
		"graphData": {
			"user_owns": {
				"0": 47,
				"1": 64,
				"2": 71,
				"3": 82,
				"-1": 46
			},
			"system_owns": { ... },
			"challenge_owns": { ... },
			"first_bloods": { ... },
			"respects": { ... }
		}
	}
}
```

`[GET]` Chart data for one year, 1-month step:
```js
https://www.hackthebox.eu/api/v4/user/profile/graph/1Y/9001
```
```json
{
	"profile": {
		"graphData": {
			"user_owns": [11, 11, 11, 11, 11, 11, 20, 27, 37, 40, 71, 71],
			"system_owns": [9, 9, 9, 9, 9, 9, 17, 25, 35, 38, 71, 71],
			"challenge_owns": [0, 0, 0, 0, 0, 0, 4, 4, 73, 84, 90, 91],
			"first_bloods": [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
			"respects": [0, 0, 0, 0, 0, 0, 2, 5, 9, 12, 17, 18]
		}
	}
}
```
#### Content

`[GET]` Content submitted by user:
```js
https://www.hackthebox.eu/api/v4/user/profile/content/9001
```
```json
{
	"profile": {
		"content": {
			"machines": [{
					"id": 196,
					"name": "Player",
					"os": "Linux",
					"machine_avatar": "\/storage\/avatars\/8a85f2aadb40bc8cf633f400d2236ef2.png",
					"difficulty": "Hard",
					"rating": "4.6",
					"user_owns": 1358,
					"system_owns": 1315
				}, ...
			],
			"challenges": [{
					"id": 129,
					"name": "Bounty Head",
					"category": "Hardware",
					"likes": 50,
					"dislikes": 0
				}, ...
			],
			"writeups": [{
					"id": 244,
					"machine_id": 192,
					"machine_avatar": "\/storage\/avatars\/ca06c447787b38ec940eb55d5c54b14c.png",
					"machine_name": "Writeup",
					"url": "https:\/\/www.youtube.com\/watch?v=g22ftc5KUFk",
					"likes": 0,
					"dislikes": 0,
					"type": "machine"
				}, ...
			]
		}
	}
}
```
#### Bloods
`[GET]` Blood wins for user:
```js
https://www.hackthebox.eu/api/v4/user/profile/bloods/9001
```
```json
{
	"profile": {
		"bloods": {
			"machines": [{
				"id": 179,
				"name": "Arkham",
				"avatar": "\/storage\/avatars\/e77b1be865e66fde51d5ca25b7d8ba61.png",
				"os": "Windows",
				"difficulty_text": "Medium",
				"user_blood": true,
				"user_blood_difference": "2h 55m 34s",
				"root_blood": true,
				"root_blood_difference": "4h 44m 27s"
				},
				{	"id": 164 ...	},
				{	"id": 175 ...	},
				{	"id": 177 ...	},
				{	"id": 179 ...	} ...
			],
			"challenges": [{
					"id": 61,
					"name": "Not Art",
					"category_name": "Stego",
					"difficulty_text": "Hard",
					"blood_difference": "1d 7h 15m"
				},
				{	"id": 64 ...	},
				{	"id": 68 ...	},
				{	"id": 94 ...	} ...
			]
		}
	}
}
```
#### Machine Attack Data [Chart]
`[GET]` Overall machine solve progress (NOTE: User owns are counted here), including categories:
```js
https://www.hackthebox.eu/api/v4/user/profile/chart/machines/attack/9001
```
```json
{
	"profile": {
		"machine_owns": {
			"solved": 25,
			"total": 168
		},
		"machine_attack_paths": {
			"Web": {
				"solved": 16,
				"total": 124,
				"avg_user_solved": 10.29
			},
			"Active Directory": { ... },
			"File Misconfiguration": { ... },
			"Outdated Software": { ... },
			"Cryptography": { ... },
			"Injection": { ... },
			"Kerberoasting": { ... },
			"CMS Exploit": { ... },
			"Sandbox Escape": { ... },
			"Network": { ... }
		}
	}
}
```
