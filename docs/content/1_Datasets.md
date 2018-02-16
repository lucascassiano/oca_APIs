# Datasets

## Get All Datasets
```
GET localhost:3000/api/v1/dataset/
```

Example of response:
```
{
	"success": true,
	"data": [
		{
			"id": "7",
			"panel_address": "admin",
			"creation_date": "2018-01-26T05:00:00.000Z",
			"sensors": {
				"name": "amg8833",
				"type": "temperature"
			},
			"start_date": "2018-01-26T06:47:30.000Z",
			"end_date": null,
			"schema": null,
			"author_id": "194",
			"name": "dataset test",
			"public": false,
			"token": null
		}
    ]
}
```

## Create Dataset
```
POST localhost:3000/api/v1/dataset
```

Example of input
```
{
	"name": "dataset test",
	"panel_address": "admin",
	"sensors":
		{
			"name":"amg8833",
			"type":"temperature"
		}
	,
	"schema":{
		"model":"string",
		"temperature":"arrayInt"
	},
	"public":false	
}
```

Example of response:
```
{
	"success": true,
	"data": []
}
```

## Read Dataset
```
GET localhost:3000/api/v1/dataset/$ID
```

example of response
```
{
	"success": true,
	"data": []
}
```

## Update Dataset
```
PUT localhost:3000/api/v1/dataset/$ID
```

example of response:
```
{
	"panel_address":"new address",
	"name": "new dataset"
}
```
## Delete Dataset
```
DEL localhost:3000/api/v1/dataset/$ID
```
example of response:
```
{
	"success": true,
	"data": []
}
```

# Permissions

## Get All permissions
```
GET localhost:3000/api/v1/dataset_permission/
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

## Create Dataset Permission
```
POST localhost:3000/api/v1/dataset_permission
```

example of input
```
{

	"developer_id":192,
	"dataset_id": 2,
	"permission": "read-write"
}
```

example of response
```
{
	"success": true,
	"data": []
}
```


## Read Dataset Permission
```
GET localhost:3000/api/v1/dataset_permission/$ID
```

example of response
```
{
	"success": true,
	"data": [
		{
			"id": "1",
			"developer_id": "192",
			"dataset_id": "6",
			"permission": "read"
		}
	]
}
```

# Data


