# shellscripit-to-dump_mongodb_into_s3
This repository contains a Bash script to automate the process of creating a MongoDB database dump and uploading it to an AWS S3 bucket. The script is designed to be flexible and easy to use by setting environment variables for all necessary configuration.

## Prerequisites

Before running the script, ensure that you have the following installed:

- [MongoDB](https://www.mongodb.com/) (for `mongodump` command)
- [AWS CLI](https://aws.amazon.com/cli/) (for interacting with S3)
- A valid AWS S3 bucket
- Access to the MongoDB database you want to back up

## Environment Variables

The script relies on environment variables for configuration. You must set the following variables:

- `MONGO_HOST`: The IP address or DNS of the MongoDB server.
- `MONGO_PORT`: The port MongoDB is running on (default is 27017).
- `MONGO_USER`: The username for MongoDB authentication.
- `MONGO_PASSWORD`: The password for MongoDB authentication.
- `MONGO_DB`: The name of the MongoDB database to back up.
- `DUMP_DIR`: The local directory where the dump file will be stored temporarily.
- `S3_BUCKET`: The S3 bucket to which the dump file will be uploaded.

To set these variables, you can either export them directly in your terminal or create a `.env` file.

### Example:

```bash
export MONGO_HOST="your_mongo_host"
export MONGO_PORT="27017"
export MONGO_USER="your_mongo_user"
export MONGO_PASSWORD="your_mongo_password"
export MONGO_DB="your_mongo_database"
export DUMP_DIR="/path/to/dump/directory"
export S3_BUCKET="s3://your-bucket-name"

To run the scripit 
