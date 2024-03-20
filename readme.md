
# URL Shortener

A little project to shorten URL with a code passed by the user.

The user would send which link he would like to make shorter and would send a word, that will work as a code for his new link.

Ex.:
- URL to be shortened: https://google.com
- Code to reference the shortened URL: test

Result:
- http://localhost:3333/test
By navigating to this result, the user is redirected to https://google.com


## Tech Stack

**Server:** Node, Fastify, Typescript, TSX

**Databases:** Postgres, Redis


## Run Locally

Clone the project

```bash
  git clone https://link-to-project
```

Go to the project directory

```bash
  cd my-project
```

Install dependencies

```bash
  pnpm install
```

Start the server

```bash
  pnpm run start
```


## Installation

Install my-project with pnpm or npm

```bash
  npm install my-project
  cd my-project
```

## API Reference

#### Get all items

```http
  GET /:code
```

| Parameter | Type     | Description                                                 |
| :---------| :------- | :---------------------------------------------------------- |
| `:code`   | `string` | A parameter the user passes to redirect to his original url |

#### Get item

```http
  GET /api/links
```

| Parameter | Type     | Description                               |
| :-------- | :------- | :---------------------------------------- |
| None      | None     | Return all the links registered in the DB |

#### Get metrics

```http
  GET /api/metrics
```

| Parameter | Type     | Description                                               |
| :-------- | :------- | :-------------------------------------------------------- |
| None      | None     | Return all the short link IDs and number of times clicked |

#### Post links

```http
  POST /api/links
```

| Parameter | Type     | Description                                                    |
| :-------- | :------- | :------------------------------------------------------------- |
| `code`    | `String` | Some name you want to give to identify your new shortened link |
| `url`     | `String` | The url you want shortened                                     |

