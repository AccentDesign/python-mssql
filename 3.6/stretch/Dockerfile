FROM        python:3.6


RUN         apt-get update \
            && apt-get -y install \
                apt-transport-https \
                curl \
            && apt-get clean

RUN         curl https://packages.microsoft.com/keys/microsoft.asc | apt-key add - \
            && curl https://packages.microsoft.com/config/debian/9/prod.list > /etc/apt/sources.list.d/mssql-release.list \
            && apt-get update \
            && ACCEPT_EULA=Y apt-get -y install \
                msodbcsql17 \
                unixodbc-dev \
            && apt-get clean