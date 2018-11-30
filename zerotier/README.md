# Information
This is docker image for zerotier.

github: https://github.com/thanhhungqb/docker-images

# Build
docker build -t thanhhungqb/zerotier .

# Run

Start:

		docker run -d --name zerotier --rm --cap-add=NET_ADMIN --cap-add=SYS_ADMIN --device=/dev/net/tun thanhhungqb/zerotier
		
Join a network with $NID (create one if you do not have)
		
		docker exec -ti zerotier /usr/sbin/zerotier-cli join $NID
		
A manually step must be done before you machine avariable on those network, admin must login to zerotier page and accept this join.



