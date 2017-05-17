# Information
This is supervisor docker image

# Build
docker build -t supervisor .

# Run
You may want to add services before run this image

		docker run -d supervisor

To add your configure

		docker run -d -v /configure/path.conf:/etc/supervisord.d/services.conf supervisor


