<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]
-->


<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/shuaiscott/spotihook">
    <img src="https://raw.githubusercontent.com/shuaiscott/spotihook/heroku/spotihook.svg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Spotihook</h3>

  <p align="center">
    Webhooks for Spotify Playlists
    <br />
    <a href="https://github.com/shuaiscott/spotihook/issues">Report Bug</a>
    ·
    <a href="https://github.com/shuaiscott/spotihook/issues">Request Feature</a>
  </p>
</p>




<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Docker

This is an example of how to list things you need to use the software and how to install them.
#### docker-compose
  ```yaml
version: "3.9"
services:
  spotihook:
    image: ghcr.io/shuaiscott/spotihook
    container_name: spotihook
    restart: always
    volumes:
      - ./spotihook.db:/usr/src/app/spotihook.db
    environment:
      - CLIENT_ID=<CLIENT_ID>
      - CLIENT_SECRET=<CLIENT_SECRET>
      - PLAYLIST_ID=<PLAYLIST_ID>
      - WEBHOOK_URL_TEMPLATE=<WEBHOOK_URL_TEMPLATE>
      - WEBHOOK_METHOD=POST
      - WEBHOOK_CONTENT_TYPE=JSON
      # OPTIONAL: - WEBHOOK_BODY_TEMPLATE=<WEBHOOK_BODY_TEMPLATE>
      - DELAY_AMOUNT=10
      - DELAY_UNIT=SECONDS
      - DEBUG=False
  ```
  
  #### Docker
  ```sh
docker run \
TODO
  ```

### Heroku

1. Create a new app on the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications)
2. Keep the `client_id` and `client_secret` handy
3. Click the Button ⬇️⬇️⬇️

   [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/shuaiscott/spotihook/tree/heroku)

4. Fill out the required parameters in Heroku and Deploy it
5. Open your app's addons and open "Heroku Scheduler" to configure it
6. Add a new job that runs this command every 10 minutes:
```sh
python spotihook.py
```
7. Profit



<!-- VARIABLE EXAMPLES -->
## Variables

| Variable | Description | Default | Required|
|----------|-------------|---------|---------|
|CLIENT_ID|Spotify client_id from the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications)|None|Yes|



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/github_username/repo_name/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.
