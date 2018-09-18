# Python 3 Base image with mssql server client drivers

for use with ``django-pyodbc-azure``

Usage:

    DATABASES = {
        'default': {
            'ENGINE': 'sql_server.pyodbc',
            'HOST': 'RDS_HOSTNAME',
            'PORT': 'RDS_PORT',
            'NAME': 'RDS_DB_NAME',
            'USER': 'RDS_USERNAME',
            'PASSWORD': 'RDS_PASSWORD',
            'OPTIONS': {
                'driver': 'ODBC Driver 17 for SQL Server',
                'MARS_Connection': 'True',
            },
        }
    }