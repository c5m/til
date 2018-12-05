# Maven Release Plugin

## release:prepare
This will
1. Check no uncomitted changes  
1. Check no dependencies on SNAPSHOT versions
2. Remove SNAPSHOT suffix from version.
3. Run tests
4. Commit and Push
5. Create tag
6. Increment version
7. Commit and Push

## release:perform
This will
1. Checkout latest tag
2. Build code
3. Deploy artifact to repository

## release:rollback
This will rollback changes made by a previous release.
Requires `release.properties` to be present (so cannot be done after a `release:clean`).