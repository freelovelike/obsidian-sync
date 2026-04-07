{

"mcpServers": {

"GVA-Helper": {

"command": "npx",

"args": [

"mcp-remote",

"http://127.0.0.1:8888/sse"

],

"env": {},

"disabled": false

},

"postgres": {

"command": "docker",

"args": [

"run",

"-i",

"--rm",

"-e",

"DATABASE_URI",

"crystaldba/postgres-mcp",

"--access-mode=unrestricted"

],

"env": {

"DATABASE_URI": "postgresql://readonly_user:readonly_pass@47.238.245.164:5433/postgres?sslmode=disable"

}

},

"mysql": {

"command": "npx",

"args": [

"-y",

"@benborla29/mcp-server-mysql"

],

"env": {

"MYSQL_HOST": "47.238.245.164",

"MYSQL_PORT": "3306",

"MYSQL_USER": "being-market-admin",

"MYSQL_PASS": "XX8DNSX5ZbFJ42RK",

"MYSQL_DB": "being-market-admin",

"ALLOW_INSERT_OPERATION": "true",

"ALLOW_UPDATE_OPERATION": "true",

"ALLOW_DELETE_OPERATION": "true"

}

}

}

}