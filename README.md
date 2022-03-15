# Full Stack kurssi osa 8 tehtävät

Linkki kurssin sivulle [GraphQL-palvelin](https://fullstackopen.com/osa8/graph_ql_palvelin).

```sh
npm init
npm install apollo-server graphql
```

Käynnistäminen:

```sh
node index.js
```

Avaa [sandbox](https://studio.apollographql.com/sandbox/explorer)

lisääminen Git:

```sh
tag="8.2"; git add .; git commit -am $tag; git tag -a $tag -m $tag; git status; git tag -l
```

Lisääminen GitHubiin:

```sh
git remote add origin https://github.com/mikakk/FullStack-part-8.git
/i/dev/2018/FullStack-kurssi/part-8-exercise$ git branch -M main
/i/dev/2018/FullStack-kurssi/part-8-exercise$ git push -u origin main
```

Pohjille tiedosto [library-backend.js](https://github.com/fullstack-hy2020/misc/blob/master/library-backend.js)

## Tehtävä 1

```GraphQL
query Query {
  bookCount
  authorCount
}
```

## Tehtävä 2

```GraphQL
query {
  allBooks {
    title
    author
    published
    genres
  }
}
```