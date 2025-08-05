<div align="center">
	<h1>ft_transcendence</h1>
	<img src="https://raw.githubusercontent.com/alissonmarcs/alissonmarcs/refs/heads/main/images/ft_transcendencem.png" alt="ft_transcendence project badge of 42"/>
	<p align="center">A 42 project where we have to create a pong game.</p>
</div>

<div align="center">
	<h2>Final score</h2>
	<img src="https://i.imgur.com/dL7Srhr.png" alt="Project scored with 125/100">
</div>

## How run

```sh
git clone https://github.com/alissonmarcs/ft_transcendence
cd ft_transcendence
./ft_transcendence setup # create .env file and certs
docker compose up
```

As the use of https is mandatory, we create two self signed certs. The first is the cert of CA, and the second is the cert of our backend, that were signed by the cert of CA. You must import the cert of CA in your browser to be able to use the site.

The file to be imported is `services/root-ca.crt`.

Steps to import in Firefox: https://javorszky.co.uk/2019/11/06/get-firefox-to-trust-your-self-signed-certificates/

When certs are done, check `IP` var  at `.env`. In your browser url bar, use `https://$IP:8080` to access the site.

## How clear

```sh
docker compose down --rmi all
./ft_transcendence setup # delete .env, service's DBs, and certs
```

