# Theatre Service

API service for theatre management written on DRF


## Getting started

1. Clone the repository

`git clone https://github.com/FanniMalevych/theatre-service.git`

2. Create virtual environment and install dependencies 

`python -m venv venv`
`venv\Scripts\activate (on Windows)`
`source venv/bin/activate (on macOS)`
`pip install -r requirements.txt`

## Run with docker

Docker should be installed
Do not forget to update .env file

`docker-compose build`
`docker-compose up`

- To populate db with test data:

`docker-compose run theatre sh -c "python manage.py loaddata theatre_data_db.json"`

- After loading data you can use following admin user:
    - Email: `admin.user@theatre.com`
    - Password: `1qazcde3`

- Create new user:
    - api/user/register

- To generate token:
    - api/user/token


## Features

- JWT authenticated
- Admin panel
- Documentation at api/doc/swagger
- List of plays, actors, performances and theatre halls
- Filtering plays and performances
- Managing orders and tickets
