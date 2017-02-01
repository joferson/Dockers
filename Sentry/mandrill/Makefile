all:
	docker build -t wpensar/postfix .
run:
	docker run --detach=true  --name postfix --publish=25:25 wpensar/postfix
clean:
	docker stop mandrill && docker rm mandrill
debug:
	docker run -i -t --volumes-from mandrill mandrill tail -f /var/log/mail.log
