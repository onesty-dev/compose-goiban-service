# compose-goiban-service

This is a docker-compose file that runs a complete environment for the goiban service by [fourcube](https://github.com/fourcube).
It's starting a MySQL container, a phpmyadmin container the [goiban container](https://hub.docker.com/r/fourcube/openiban/) and a [data loader container](https://hub.docker.com/r/onesty/goibandataloader/).

It also loads a database initialisation script located at mysql/.docker/build-resources/goiban.sql

The data loader container can be configured by the following environment variables:

* EXCEL_TO_DATABASE_JOB_CRON (default 0 0 0 25 12 ?)
* SPRING_DATASOURCE_URL (default jdbc:mysql://localhost:3306/goiban)
* EXCEL_FILE_DELETE (default true)
