# Welcome to sillyanimal.github.io
A database of many skyblock members of interest.

## USAGE
Make a `GET` request to `https://sillyanimal.github.io/{username}.json`
Where `{username}` is the username of the user you want to recieve data on.

Python example:
```py
import requests

def main(username):
    url = "https://sillyanimal.github.io"
    result = requests.get(f"{url}/{username}.json")
    if result.status_code == 404:
        print(f"No entry for user '{username}'")
    else:
        print(f"Information for '{username}':")
        json = result.json()
        for key in json:
            print(f"{key}: {json[key]}\n")

username = input("Enter member username > ")
while username != "exit":
  main(username)
  username = input("Enter member username > ")
``` 

## CONTRIBUTING
Have information you want to add? Modlogs not mentioned? A member missing? Contact `lokisolos#0000` on discord to request an edit.
