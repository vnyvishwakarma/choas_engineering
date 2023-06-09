# Choas Engineering

## History 

![history](images/history.png)

## What is Chaos Engineering 

![chaos](images/chaos.png)


## How to Install the Chaos Toolkit


### Install Python for your system:

On MacOS X:


```bash
  brew install python3
```

Create a virtual environment:

```bash
  python3 -m venv ~/.venvs/chaostk
```

Make sure to always activate your virtual environment before using it:

```bash
  source  ~/.venvs/chaostk/bin/activate
```


### Install chaostoolkit in the virtual environment as follows:

```bash
  pip install -U chaostoolkit
```

You can verify the command was installed by running:

```bash
  chaos --version
```


## Applcation Overview 


![application](images/app.png)

Run application which is made of two microservices (astre.py and sunset.py) that converse with each other over HTTPS

Installing requirements:

```bash
  pip install -r ./sample-app-code/requirements.txt
```

Note: Make sure to always activate your virtual environment before using it ==> 

```bash
  source  ~/.venvs/chaostk/bin/activate
```

Run both micrservices in background :

```bash
python3 ./astre.py &
```
```bash
python3 ./sunset.py &
```

test using curl command or postman


```bash
curl -k https://localhost:8443/city/paris
```

```bash
chaos run experiment.json
```

```bash
chaos run --rollback-strategy always experiment.json 
```


Chaos engineering, a dance of disorder, We test and we break, to build systems stronger.



