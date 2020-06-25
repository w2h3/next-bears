# Migration `20200624070514-create-sighting`

This migration has been generated by Leigh Halliday at 6/24/2020, 7:05:14 AM.
You can check out the [state of the schema](./schema.prisma) after the migration.

## Database Steps

```sql
CREATE TABLE "public"."Sighting" (
"createdAt" timestamp(3)  NOT NULL DEFAULT CURRENT_TIMESTAMP,"id" SERIAL,"latitude" Decimal(65,30)  NOT NULL ,"longitude" Decimal(65,30)  NOT NULL ,
    PRIMARY KEY ("id"))
```

## Changes

```diff
diff --git schema.prisma schema.prisma
migration ..20200624070514-create-sighting
--- datamodel.dml
+++ datamodel.dml
@@ -1,0 +1,18 @@
+// This is your Prisma schema file,
+// learn more about it in the docs: https://pris.ly/d/prisma-schema
+
+datasource db {
+  provider = "postgresql"
+  url = "***"
+}
+
+generator client {
+  provider = "prisma-client-js"
+}
+
+model Sighting {
+  id        Int      @id @default(autoincrement())
+  createdAt DateTime @default(now())
+  latitude  Float
+  longitude Float
+}
```

