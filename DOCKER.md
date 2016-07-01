# Docker instructions

## How to build

	docker build -t blur-admin .
	
## How to run

For development:

	docker run -p 3000:3000 blur-admin
	
For production:

	docker run -p 3000:3000 -e "GULP_COMMAND=serve:dist" blur-admin
	
## How to customise

1. Create a new Dockerfile with 

	FROM blur-admin

2. Add the following line to then copy in any customised files

	COPY $(MY_SOURCE_FOLDER) /usr/src/app/src
