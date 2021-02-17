# Install on Ubuntu for CLI

## Create the file repository configuration:

    sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

## Import the repository signing key:

    wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

## Update the package lists:

    sudo apt-get update

    # Install the latest version of PostgreSQL.
    # If you want a specific version, use 'postgresql-12' or similar instead of 'postgresql':

    sudo apt-get -y install postgresql

## Change Password

For most systems, the default Postgres user is postgres and a password is not required for authentication. Thus, to add a password, we must first login and connect as the postgres user.

    sudo -u postgres psql

With a connection now established to Postgres at the psql prompt, issue the ALTER USER command to change the password for the postgres user:

    postgres=# ALTER USER postgres PASSWORD 'myPassword';
    ALTER ROLE

Exit postgres user

    postgres=# \q
