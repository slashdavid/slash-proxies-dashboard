# Recovering files from a MongoDB Atlas snapshot

In order to access the customer files that were in the Atlas snapshot, I had to utilize MongoDB's Community Server, Tools package, and Shell.

Using these technologies, I was able to:
1. Locally host a database on my PC
2. Execute a WiredTiger -> BSON dump
3. Restore all customer data onto database

# 1. Locally host a database on my PC
To start, I had to move copies of the files in the Atlas snapshot into my local dbPath folder (C:\data\db). I wasn't able to simply open these files as they were all under the .wt file type. This stands for WiredTiger. It's a file type that is exclusive to MongoDB and isn't something you would normally manipulate by itself.

Afterwards, I'm now permitted to run the `mongod` command, which launches a MongoDB daemon in the background

# 2. Executed a WiredTiger -> BSON dump
Now that the daemon is running, I'm able to execute `mongodump --out <desired_path_for_bson_files>`, which creates BSON backup files of the database files located in my local dbPath.

# 3. Restore all customer data onto database
For this step, I simply had to deploy a basic MongoDB Atlas M0 cluster, which will act as my new database.

Once this has been done, I'm permitted to run this command: `mongorestore --db <database_name> <path_to_bson_files>`. This mongorestore command uses the BSON files I got from the dump and uploads them into the new database.

Following this, I can finally run this command to effectively convert customers.bson to customers.json: `mongoexport --db <database_name> --collection customers.bson --out <output_file_path> --jsonArray`.
