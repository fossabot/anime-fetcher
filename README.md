# anime-fetcher
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fyuyuvn%2Fanime-fetcher.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fyuyuvn%2Fanime-fetcher?ref=badge_shield)


## Install & deploy

1. Go to https://console.developers.google.com/apis/credentials
2. Go to OAuth consent screen
3. Set Email address and Product name shown to users
4. Create OAuth client ID -> Other
5. Download OAuth 2.0 client ID as json, rename it to client_secret.json then move to current folder
6. `node getToken.js`
8. `node index.js`
9. Each time there are a post request to http://localhost:5321/fetch/:spreadsheets_id it will fetch new ep from horriblesubs

Request content type must be json. Body must have bittorrent_url param which contain bittorent url.
```json
{
  "bittorrent_url": "http://admin:password@192.168.1.1:9090"
}
```

## Exam spreadsheet file
Sheet name MUST be `Ongoing`. First column is url to anime, second column is current newest episode.

| Url | Episode |
| --  | -- |
| http://horriblesubs.info/shows/comic-girls	| 10 |
| http://horriblesubs.info/shows/steins-gate-0	| 9 |
| http://horriblesubs.info/shows/amanchu-advance	| 10 |
| http://horriblesubs.info/shows/megalo-box	| 10 |


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fyuyuvn%2Fanime-fetcher.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fyuyuvn%2Fanime-fetcher?ref=badge_large)