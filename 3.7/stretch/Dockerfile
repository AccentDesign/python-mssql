FROM        python:3.7

# Install SQL server dependencies and drivers
RUN         apt-get update \
            && apt-get install -y \
                apt-transport-https \
                curl \
            && curl https://packages.microsoft.com/keys/microsoft.asc | apt-key add - \
            && curl https://packages.microsoft.com/config/debian/9/prod.list > /etc/apt/sources.list.d/mssql-release.list \
            && apt-get update \
            && ACCEPT_EULA=Y apt-get install -y \
                msodbcsql17 \
                unixodbc-dev
