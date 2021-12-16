## Usage

To get started with the code examples, start Airflow with Docker Compose with the following command:

```bash
docker-compose up -d
```

The webserver initializes a few things, so wait for a few seconds, and you should be able to access the
Airflow webserver at http://localhost:8080.

To stop running the examples, run the following command:

```bash
docker-compose down -v
```

## Intro to Airflow

Let's build a basic pipeline to fetch information about rocket launches, save them locally and then notify you when the task is complete.

1. Use [The Space Devs API](https://thespacedevs.com/llapi), with the url, https://ll.thespacedevs.com/2.0.0/launch/upcoming/ will help you get all the data you need.
2. Within the Docker container save the data to the postgres database or to a `tmp` file. You could save the images locally or to the database.
3. Send a basic message in the form of a bash command to notify you about the end of the pipeline.

### Improvements

If you have the time on your own try doing the following:

1. Save the data to an S3 bucket
2. Send notifications using email or slack
