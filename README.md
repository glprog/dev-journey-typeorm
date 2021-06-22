### Create a migration
- typeorm migration:create -n {migrationName}
### Run migrations
- typeorm migration:run
### Column with uuid in PostgreSQL
``` json
{
  "isPrimary": true,
  "name": "id",
  "type": "uuid",
  "generationStrategy": "uuid",
  "default": "uuid_generate_v4()",
}
```
Before use ```uuid_generate_v4()``` you should execute this command bellow
``` javascript
await queryRunner.query(`CREATE EXTENSION IF NOT EXISTS "uuid-ossp"`);
```
