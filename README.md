# Spotify - Infra As Code using Terraform

Create a playlist on Spotify by writing it as a Terraform configuration.

## Required

- [x] [Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli) Installed
- [x] [Docker](https://docs.docker.com/desktop/)
- [x] [Spotify Developer Account](https://developer.spotify.com/dashboard/login)

## Dependency

* Develop an Spotify Authorization server for Manage Tokens

# Project Structure

| **File** | **Description** |
| :---: | :---: |
| [main.tf](main.tf) | Manage the resouce |
| [versions.tf](versions.tf) | Require provider version |
| [variables.tf](_variables.tf) | retrieve variable |
| [defaults.tf](_defaults.tf) | define the values on vars |
| [provider.tf](_provider.tf) | Set provider |
| [backend.tf](_backend.tf) | Search tracks |
| [output.tf](_output.tf) | obtain the result |

## Before Try

Set environment.

```bash
export SPOTIFY_CLIENT_REDIRECT_URI=http://localhost:27228/spotify_callback
```

## Usage

```bash
# Initializing the backend for Generate Playlist
 terraform init
```
Please you need to check if you authorize your application
Don't run the next command without the previous authorization or this probably will fail

```bash
# Terraform will perform the action on resource
terraform apply
```

## Result

After succeed those commands your output, should be return your playlist.
Then you may check on [Spotify Search](https://open.spotify.com/search).

Find by the name of your playlist and thats it

## Reference
Follow along with the tutorial at [learn.hashicorp.com](https://learn.hashicorp.com/tutorials/terraform/spotify-playlist).

## Credits
[HashCorp GitHub](https://github.com/hashicorp/learn-terraform-spotify)