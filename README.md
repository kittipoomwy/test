# FastAPI Server Application for Recommended Restaurants

This project is created for recommending restaurants for users by their feeatures.

## Dependencies to install

- [Python 3.12]
- [Pip]
- [Docker]
- [Docker Compose]


## Setup

In order to run the server application locally, you may or may not change the data for postgreSQL in .env file.

- `.env`

To run the application in docker, run the following command:

```bash
docker-compose up --build
```

## Databases

This database aim to get recommended restaurants by user's features and user's coordinates

- `[GET] /recommend/{user_id}?latitude=<user_latitude>&longitude=<user_longitude>&size=<max_restaurants>&max_dis=<max_displacement>&sort_dis=<1_for_by_displacement_or_2_for_by_dictance>` : returns user's value
- `[POST] /recommend/{user_id}?latitude=<user_latitude>&longitude=<user_longitude>&size=<max_restaurants>&max_dis=<max_displacement>&sort_dis=<1_for_by_displacement_or_2_for_by_dictance>` : returns user's value
  - size is optional, default value is 20
  - max_dis is optional, default value is 5000
  - sort_dis is optional, default value is 1

## Testing

For testing purposes, locust is used. The tests are located in `./tests` folder

## Requirements
The project uses Python 3.12. This is a list of required libraries:
```python
fastapi==0.115.7
sqlalchemy==2.0.37
pandas==2.1.2
pyarrow==14.0.0
scikit-learn==1.3.2
numpy==1.26.1
geopy==2.4.1
uvicorn==0.34.0
psycopg2==2.9.10
python-dotenv==1.0.1
cachetools==5.5.1
```

