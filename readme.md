

# Instructions

## Clone the project

```
git clone https://github.com/weaviate-tutorials/rbac.git
```

## Setup python environment

```
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Configure the docker image and run

First, follow the instructions from your DX guide, and update environment variables in [docker-compose.yml](./docker-compose.yml)

See [docs - RBAC: Docker](https://v1-29-rbac--tangerine-buttercream-20c32f.netlify.app/developers/weaviate/configuration/authorization#rbac-docker)

Focus on:
**Configure Users with API keys**
* `AUTHENTICATION_APIKEY_ENABLED` – enables auth with API keys, set to true
* `AUTHENTICATION_APIKEY_USERS` - a list of userIDs
* `AUTHENTICATION_APIKEY_ALLOWED_KEYS` - a list of API keys for each of the above userID

**Configure RBAC**
* `AUTHORIZATION_RBAC_ENABLED` - enables RBAC, set to true
* `AUTHORIZATION_RBAC_ROOT_USERS` - a list of user_ids that have Admin/Root permissions. Root users can create new roles, manage their permissions and assign them to users.

When ready, run:
```
docker compose up -d
```

## Work through the 2 notebooks
Follow instructions from your DX guide.