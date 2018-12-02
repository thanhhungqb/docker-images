# Information
This is docker image for rclone.

github: https://github.com/thanhhungqb/docker-images

For more information about rclone here: https://rclone.org

# Build
		docker build -t thanhhungqb/rclone .

For Raspbian version, please run with Dockerfile.rpi:

		docker build -t thanhhungqb/rclone:rpi -f Dockerfile.rpi .
# Run

In most case, we use it as a command, and for persistent configure, we mount a config directory outside by -v

Start:

		docker run -ti --rm --name rclone thanhhungqb/rclone bash
		
With mount configure folder (persistent configure):
		
		docker run -ti --rm --name rclone -v `echo $HOME/.config`/rclone:/root/.config/rclone thanhhungqb/rclone rclone config
		

Alias for easy to use:
		alias rclone='docker run -ti --rm --name rclone -v `echo $HOME/.config`/rclone:/root/.config/rclone thanhhungqb/rclone rclone'


