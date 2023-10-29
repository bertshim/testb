# Drum Penguin
![drum_penguin-small](https://github.com/bertshim/Drum-Penguin/assets/5170244/d565987b-69a2-4a53-ac05-706c591c2f74)

Drum Penguin presents an effortless solution for establishing RESTful CRUD API servers.
You can download the executable binaries from this repository, along with some usage examples.

### The official Home page:
https://drumpenguin.weebly.com/

# 🚀 Concept
Drum Penguin is not just a library or framework; it is a full-fledged server designed for production environments. 
It reads the database connection string from the 'config.json' file and operates as a CRUD server for the database immediately. 
You can utilize it during both the development and production phases

# ⚡ Performance 
Drum Penguin is built on top of a functional language.
It is robust and generally delivers better performance with MySQL/MariaDB compared to Node.js counterparts, 
which are well known for their high performance.⏳

Check this benchmarking report. Drum Penguin is built with Elixir(cowboy).

https://stressgrid.com/blog/benchmarking_go_vs_node_vs_elixir/ ⚡ 

# 🎯 Installation

Clone this repository.

```console
git clone https://github.com/bertshim/drum_penguin.git
```

## Windows
```console
cd bin\win
```
## Linux
For Ubuntu, CentOS an most Linux on x86 or AMD64 architecures.
```console
cd bin/linux
```
## Linux (ARM)
For Ubuntu, CentOS an most Linux on ARM architecures.
(Tested on AWS instances on ARM chips)
```console
cd bin/linux_arm
```

# 🛠Setup a database connection 
Open the config.json in the path above, according to your OS and architecture.
Edit the connection information.

```json
{
  "connection": {
    "hostname": "my_host",
    "username": "my_port",
    "password": "my_pass",
    "database": "my_database",
    "port" : 3306
  }
}
```
By configuring this connection information, Drum Penguin generates RESTful APIs for all tables in the database

# 🚗 Run

## Windows
```console
drum_penguin.bat
```
## Linux
For Ubuntu, CentOS an most Linux on x86 or AMD64 architecures.
```console
./drum_penguin.sh
```
## Linux (ARM)
For Ubuntu, CentOS an most Linux on ARM architecures.
(Tested on AWS instances on ARM chips)
```console
./drum_penguin.sh
```

# 🎨 Usage
RESTful APIs by Drum Penguin are generated based on your tables and columns. For example, if you have a table like USERS:

### Table : USERS
| id | name    | major    | address      |
|--- |---      |---       |---           |
| 1  | Issac   | Physics  | Lincolnshire |
| 2  | Albert  | Physics  | Ulm          |
| 3  | Alan    | Math     | London       |


## GET
Fetch a row from users, where the name is "Issac"
```console
http://localhost:7077/users/name/Issac 
```

## POST
Create a data in users, with POST body as a Json string
```console
http://localhost:7077/users
```
Body:
```console
{"name": "Tim", "major": "Computer", "address": "LA"} 
```

## PUT (Update)
Update a row in users, with PUT body as a Json string
```console
http://localhost:7077/users/name/Issac
```
Body:
```console
{"major": "Math", "address": "London"}
```

## DELETE
Delete a row in users, where name is "Issac"
```console
http://localhost:7077/users/name/Issac
```

![small-happy-penguin](https://github.com/bertshim/Drum-Penguin/assets/5170244/82410516-b1cb-428e-ae1f-941707de32ae)

# 🍦 Enjoy Drum Penguin !

