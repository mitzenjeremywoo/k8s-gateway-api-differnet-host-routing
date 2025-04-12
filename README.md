
Create the gateway and http routes

k apply -f gateway.yaml

k apply -f httproute-A.yaml

k apply -f httproute-B.yaml

Get the ip address of your gateway using the following command: 

k get gateway 

Then curl the services

curl --resolve a.example.com:80:35.213.245.4 http://a.example.com

Then curl the services

curl --resolve b.example.com:80:35.213.245.4 http://b.example.com

