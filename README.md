# Fauna Action

This action gives you the ability to manage your Fauna resources in the CI/CD pipeline through Fauna Schema Language. Using this action you are able to

- create, update, delete databases
- manage collections
- manage user defined function
- manage database access
- automate integration testing

# How to use it

Create a new fauna schema file (i.e. `myshema.fsl`) in your project. Add the github action as a step as follows

```yml
# ...
steps:
  - name: run fauna_db_actions
    uses: Shadid12/fauna-action@0.0.7
    with:
      node-version: '20'
      fauna-secret-key: ${{ secrets.FAUNA_SECRET_KEY }}
      schema-directory: './'
```

### With pnpm

```yml
# ...
steps:
  - name: run fauna_db_actions
    uses: Shadid12/fauna-action@0.0.7
    with:
      ...
      package-manager: pnpm
      ...
```

Based on the schema the action will apply the changes in your database.
