# snapshotanalyzer

Project to manage the AWS EC2 instance snapshots

## About

This project uses boto3 to manage AWS EC2 instance snapshots.

## Configuring

shotty uses the configuration file created by the AWS cli. e.g.

`aws configure --profile shotty`

## Running

`pipenv run "pyhon shotty/shotty.py"`

## Docs

http://boto3.readthedocs.io/en/latest/reference/services/ec2.html
```
pipenv run ipython
import boto3
session = boto3.Session(profile_name='shotty')
ec2 = session.resource('ec2')
inst = ec2.instances.all()
inst
list(inst)
list(inst)[0]
i = list(inst)[0]
i.id
i.placement
i.state
```
