TP Tests IHM
==================

## Objectifs

Durant ce TP, nous allons implémenter un test de bout-en-bout en utilisant le framework Cypress.

## Pré-requis
- [Node 6+](https://nodejs.org/)
- [git](https://git-scm.com)

```bash
git clone git@github.com:fla-kata/cypress.git
cd cypress
npm install
```

Puis installer les dépendances de l'application :
```bash
cd todomvc
npm install
```

## Découvrir l'application à tester

### Faire tourner l'application
```bash
cd todomvc
npm start

```

Ouvrir un navigateur sur localhost:3000

### Examiner le code (brièvement)

Ouvrir le fichier todomvc/index.html

## Mise en place test simple

### Structure

```bash
cd /tmp
mkdir example
cd example
npm init --yes
npm install -D cypress
```

Puis l'une des deux commandes :

```bash
$(npm bin)/cypress open
./node_modules/.bin/cypress open
```

Explorons la structure :

- "cypress.json" - all Cypress settings
- "cypress/integration" - test files (specs)
- "cypress/fixtures" - mock data
- "cypress/plugins" - extending Cypress
- "cypress/support" - shared commands, utilities

### test lecture

Pour ce 1er, votre mission sera de corriger le test suivant ; en cherchant dans la documentation à comprendre ce qui se déroule.

Créer le fichier `cypress/integration/spec.js` avec le contenu suivant :

```
it('loads', () => {
  cy.visit('localhost:3000')
  cy.contains('h1', 'Todos App')
})
```

La documentation est votre [meilleure amie](https://docs.cypress.io/)

**Questions :**

- pourquoi la commande échoue ?
- comment corriger ?
- comment pouvez-vous sélectionner un élément ?
- imaginer les tests à réaliser sur cette application

### tests ajout

Nous souhaitons :
- vérifier que la liste est vide au démarrage (cy.get, should('have.length', ...),
- ajouter un TODO et vérifier que la liste est correcte (cy.get, cy.type, cy.contains)



