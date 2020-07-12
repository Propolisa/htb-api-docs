---
layout: page
title: Self
parent: Home
nav_order: 1
---

<img src="https://app.hackthebox.eu/images/icons/ic-icons-kickass/ic-vip-big.svg" style="max-width:128px;float:right;" />

## Data about yourself

Want to keep track of your own progress, achievements or other account matters? These are the endpoints for you. 

<span class="label label-green">GET</span>
Get profile info (self):
```js
/api/v4/user/info
```
`🥙 RESPONSE`
```json
{
	"info": {
		"id": 9001,
		"name": "L33tUser",
		"email": "l33t@email.com",
		"timezone": "UTC",
		"isVip": true,
		"canAccessVIP": true,
		"isServerVIP": true,
		"server_id": 222,
		"avatar": "\/storage\/avatars\/e6baffa3faa.png"
	}
}
```


<span class="label label-green">GET</span>
Get VPN connection status info (self):

```js
/api/v4/user/connection/status
```
`🥙 RESPONSE`
```json
{
	"status": "1",
	"connection": {
		"name": "Username",
		"ip4": "10.10.14.50",
		"ip6": "dead:beef:2::100a",
		"down": "0.09",
		"up": "0.08"
	}
}
```

<span class="label label-green">GET</span>
Get your own running machine instance (VIP):

```js
/api/v4/machine/active
```
`🥙 RESPONSE`
```json
{
	"info": {
		"id": 244,
		"name": "Quick",
		"avatar": "\/storage\/avatars\/c2096057971181c8d36031fb6f1f7a8a.png",
		"expires_at": "2020-07-08 14:14:53",
		"voting": false,
		"voted": false
	}
}
```

<span class="label label-green">GET</span>
Get machines you marked as **TODO**, if any:

```js
/api/v4/machine/todo
```
`🥙 RESPONSE`
```json
{
	"info": [ "... an array of standard machine objects ..." ]
}
```

<span class="label label-green">GET</span>
Get challenges you marked as **TODO**, if any:

```js
/api/v4/challenge/todo
```
`🥙 RESPONSE`
```json
{
	"info": [ "... an array of standard challenge objects ..." ]
}
```

<span class="label label-green">GET</span>
Retrieve your anonymized ID:

```js
/api/v4/user/anonymized/id
```
`🥙 RESPONSE`
```json
{"id":"0bb526172123027df47df67cb6d032db"}
```

## Update Operations

### Owning stuff

<span class="label label-purple">POST</span>
Submit / own a challenge flag:
```js
/api/v4/challenge/own
```
`🛍️ PAYLOAD` 
```json
{"flag":"4556","challenge_id":131,"difficulty":50}
```
`🥙 RESPONSE(S)`
```json
{"message":"Incorrect flag"}
```

<span class="label label-purple">POST</span>
Submit / own a machine flag:
> (Flags here are not real ones for obvious reasons!)
```js
/api/v4/machine/own
```
`🛍️ PAYLOAD(S)` 
```json
{"flag":"r3523452345","id":244,"difficulty":20}
```
```json
{
	"flag": "2339393e949af088314cb027b65f4bcc",
	"id": 244,
	"difficulty": 30
}
```
`🥙 RESPONSE(S)`
```json
{"message":"Incorrect flag!"}
```

```json
{
	"message": "Multimaster user is now owned.",
	"id": 232,
	"own_type": "user"
}
```

```json
{
	"message": "Quick root is now owned.",
	"id": 244,
	"own_type": "root"
}
```

### Marking Todos

<span class="label label-purple">POST</span>
`Toggle` a machine's 'todo' status:
```js
/api/v4/machine/todo/update/260
```
`🛍️ PAYLOAD` 
```diff
- No parameters for this request (machine ID specified in url).
```
`🥙 RETURNS`
> _A list of the challenges currently marked as 'todo'_
```json
{
	"info": [{
		"id": 260,
		"name": "RopeTwo",
		"os": "Linux",
		"points": 50,
		"static_points": 50,
		"authUserInUserOwns": null,
		"authUserInRootOwns": null,
		"authUserFirstUserTime": null,
		"authUserFirstRootTime": null,
		"stars": "4.2",
		"difficulty": 94,
		"feedbackForChart": {
			"counterCake": 1,
			"counterVeryEasy": 0,
			"counterEasy": 0,
			"counterTooEasy": 0,
			"counterMedium": 0,
			"counterBitHard": 0,
			"counterHard": 1,
			"counterTooHard": 0,
			"counterExHard": 0,
			"counterBrainFuck": 17
		},
		"feedbackForChartArr": [1, 0, 0, 0, 0, 0, 1, 0, 0, 17],
		"avatar": "/storage/avatars/c2847af85c98ff1b15a75aec060fa2de.png",
		"difficultyText": "Insane",
		"playInfo": {
			"isSpawned": false,
			"isActive": null,
			"active_player_count": null,
			"expires_at": null
		},
		"free": true,
		"release": "2020-06-27T16:00:00.000000Z",
		"user_owns_count": 14,
		"root_owns_count": 7,
		"recommended": 0
	}, {
		"id": 262,
		"name": "SneakyMailer",
		"os": "Linux",
		"points": 30,
		"static_points": 30,
		"authUserInUserOwns": null,
		"authUserInRootOwns": null,
		"authUserFirstUserTime": null,
		"authUserFirstRootTime": null,
		"stars": "0.0",
		"difficulty": 50,
		"feedbackForChart": {
			"counterCake": 0,
			"counterVeryEasy": 0,
			"counterEasy": 0,
			"counterTooEasy": 0,
			"counterMedium": 0,
			"counterBitHard": 0,
			"counterHard": 0,
			"counterTooHard": 0,
			"counterExHard": 0,
			"counterBrainFuck": 0
		},
		"feedbackForChartArr": [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
		"avatar": "/storage/avatars/5f5ab2f3fb31673d80623bdd98b286c3.png",
		"difficultyText": "Medium",
		"playInfo": {
			"isSpawned": false,
			"isActive": null,
			"active_player_count": null,
			"expires_at": null
		},
		"free": true,
		"release": "2020-07-11T16:00:00.000000Z",
		"user_owns_count": 0,
		"root_owns_count": 0,
		"recommended": 0
	}]
}
```

<span class="label label-purple">POST</span>
`Toggle` a challenge's 'todo' status:
```js
/api/v4/challenge/todo/update/75
```
`🛍️ PAYLOAD` 
```diff
- No parameters for this request (machine ID specified in url).
```
`🥙 RESPONSE(S)`
> _A list of the challenges currently marked as 'todo'_
```json
{
	"info": [{
		"id": 75,
		"name": "Fuzzy",
		"difficulty": "Easy",
		"points": 0,
		"difficulty_chart": {
			"counterCake": 752,
			"counterVeryEasy": 1222,
			"counterEasy": 4681,
			"counterTooEasy": 2753,
			"counterMedium": 1657,
			"counterBitHard": 531,
			"counterHard": 240,
			"counterTooHard": 48,
			"counterExHard": 22,
			"counterBrainFuck": 93
		},
		"difficulty_chart_arr": [752, 1222, 4681, 2753, 1657, 531, 240, 48, 22, 93],
		"solves": 11962,
		"authUserSolve": true,
		"likes": 3123,
		"likeByAuthUser": false,
		"dislikes": 138,
		"dislikeByAuthUser": false,
		"isCompleted": true,
		"isActive": false,
		"release_date": "2019-07-05",
		"challenge_category_id": 5,
		"retired": 1,
		"recommended": 0
	}]
}
```

### VIP

<span class="label label-purple">POST</span>
Spawn a new instance of the identified machine:
```js
/api/v4/vm/spawn
```
`🛍️ PAYLOAD` 
```json
{"machine_id":262}
```
`🥙 RESPONSE(S)`
```json
{"message":"Machine not available for VIP."}
```
```json
{"message":"Machine deployed to lab."}
```

<span class="label label-purple">POST</span>
Extend a running instance of the identified machine:
```js
/api/v4/vm/spawn
```
`🛍️ PAYLOAD` 
```json
{"machine_id":244}
```
`🥙 RESPONSE(S)`
```json
{
	"message": "Machine extended by 24 hours.",
	"expires_at": "2020-07-09T21:52:24.093483Z"
}
```
```json
{"message":"Machine not found."}
```
```json
{"message":"Machine not assigned to this lab."}
```