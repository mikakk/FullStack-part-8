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
tag="8.2-1"; git add .; git commit -am $tag; git tag -a $tag -m $tag; git push; git status; git tag -l; 
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
query {
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

## Tehtävä 3

```GraphQL
query {
  allAuthors {
    name
    bookCount
  }
}
```

## Tehtävä 4

```GraphQL
query {
  allBooks(author: "Robert Martin") {
    title
  }
}
```

## Tehtävä 5

```GraphQL
query {
  allBooks(genre: "refactoring") {
    title
    author
  }
}
```

```GraphQL
query {
  allBooks(author: "Robert Martin", genre: "refactoring") {
    title
    author
  }
}
```

## Tehtävä 6

Lisää uusi kirja olemassa olevalle kirjailijalle:  

```GraphQL
mutation {
  addBook(
    title: "NoSQL Distilled",
    author: "Martin Fowler",
    published: 2012,
    genres: ["database", "nosql"]
  ) {
    title,
    author
  }
}
```

Lisää uusi kirja ja kirjailija:  

```GraphQL
mutation {
  addBook(
    title: "Einari",
    author: "Antti Heikkinen",
    published: 2020,
    genres: ["biography"]
  ) {
    title,
    author
  }
}
```
