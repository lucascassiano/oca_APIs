## Get All Panels
```
GET oca.media.mit.edu/api/v1/panel/
```

Example of response:
```
{
	"success": true,
	"data": [
		{
			"id": "37",
			"panel_id": "1",
			"creation_date": "2018-02-15T05:00:00.000Z",
			"devices": {
				"name": "amg8833",
				"type": "sensor",
				"category": "temperature"
			},
			"start_date": "2018-02-15T09:37:23.000Z",
			"end_date": null,
			"data_schema": {
				"model": "string",
				"temperature": "arrayInt"
			},
			"author_id": "194",
			"name": "dataset test",
			"public": true,
			"hash": "84f334b2b15b0bbf02dbc7ae7177443e",
			"comment": null
		}
	]
}

```

## Create Panel ```(Admin only)```
```
POST oca.media.mit.edu/api/v1/dataset
```

Example of input
```
{
	"position":{
		"x": 0,
		"y": 0,
		"z": 0
	},
	"ip_address":"127.0.0"
}
```

Example of response:
```
{
	"success": true,
	"data": []
}
```

## Read Panel
```
GET oca.media.mit.edu/api/v1/panel/$ID
```

example of response
```
{
	"success": true,
	"data": {
		"id": "1",
		"position": {
			"x": 0,
			"y": 10,
			"z": 0
		},
		"ip_address": "127.0.0",
		"hash": "886c21d2aed76f69fa93ccffba49e118"
	}
}
```

## Update Panel ```(Admin only)```
```
PUT oca.media.mit.edu/api/v1/panel/$ID
```

example of response:
```
{
	"success": true,
	"data": []
}
```
## Delete Dataset ```(Admin only)```
```
DEL localhost:3000/api/v1/panel/$ID
```
example of response:
```
{
	"success": true,
	"data": []
}
```

# Datasets related to Panel
This will expose only the datasets visible for the developer. e.g. if the dataset is set as ```public```, permissions are ```read``` or ```read-only```.

## Get all visible datasets indexed to a specific panel
```
GET oca.media.mit.edu/api/v1/$ID/datasets/
```

example of response

```
{
	"success": true,
	"data": [
		{
			"id": "12",
			"developer_id": "192",
			"dataset_id": "7",
			"permission": "read-write"
		}
        ...
	]
}
```
