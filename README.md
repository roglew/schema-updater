Python Schema Updater
=====================

This is a python script that can be used to maintain a database schema. It imports all the schema_*.py files (where * is a number) and runs the update() function defined in it to update the schema. The update.py script uses the get_schema_version() to get the current version, and it's your responsibility to define this function since it's dependent on how you keep track of your schema.

So tl;dr:
1. Download the script and put it in its own folder
2. Define get_schema_version() in update.py
3. Create schema_n.py files which define an update() function to update from schema version n-1 to version n
4. Run update.py  (or import update.update_schema() and run it) whenever you want to update the schema
