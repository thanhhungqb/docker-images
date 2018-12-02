# Information
This is docker image for zerotier.

github: https://github.com/thanhhungqb/docker-images

ZeroTier delivers the capabilities of VPNs, SDN, and SD-WAN with a single system, more information https://www.zerotier.com/

# Build
		docker build -t thanhhungqb/zerotier .

For Raspbian version, please run with Dockerfile.rpi:

		docker build -t thanhhungqb/zerotier:rpi -f Dockerfile.rpi .
# Run

Start:

		docker run -d --name zerotier --restart=always --net=host --cap-add=NET_ADMIN --cap-add=SYS_ADMIN --device=/dev/net/tun thanhhungqb/zerotier
		
Join a network with $NID (create one if you do not have)
		
		docker exec -ti zerotier /usr/sbin/zerotier-cli join $NID
		
A manually step must be done before you machine avariable on those network, admin must login to zerotier page and accept this join.



