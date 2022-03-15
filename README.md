# Full Stack kurssi osa 8 tehtävät

Linkki kurssin sivulle [GraphQL-palvelin](https://fullstackopen.com/osa8/graph_ql_palvelin).

```sh
npm init
npm install apollo-server graphql
```

Käynnistäminen `node index.js`  
Avaa [sandbox](https://studio.apollographql.com/sandbox/explorer)

Git lisääminen:  

```Bash
git add .; git tag -a "8.2" -m "8.2"; git commit -am "8.2"; git status; git tag -l
```

Pohjille tiedosto [library-backend.js](https://github.com/fullstack-hy2020/misc/blob/master/library-backend.js)

## Tehtävä 1

```GraphQL
query Query {
  bookCount
  authorCount
}
```