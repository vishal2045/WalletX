- Clone the repo

````jsx
git clone url

- yarn
- Run postgres either locally or on the cloud (neon.tech)

```jsx
docker run  -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
````

- Copy over all .env.example files to .env
- Update .env files everywhere with the right db url
- Go to `packages/db`
  - npx prisma migrate dev
  - npx prisma db seed
- Go to `apps/user-app` , run `yarn run dev`
- Try logging in using phone - 1111111111 , password - alice (See `seed.ts`)
- Go to `packages/db` in second terminal
  - npx prisma studio
- Go to `apps/bank-webhook` , run `yarn run dev`
- Go to Postman, send Post request with userId `1`,amount and token according to the under processing transfer in prisma studio.
