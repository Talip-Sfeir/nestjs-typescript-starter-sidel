## Test Technique sur NestJS

### Coder un CRUD avec NestJS (≃ 30 min)

Mettez en place un service CRUD pour une entité "Task" dans une application NestJS. L'entité "Task" doit avoir les propriétés suivantes : 
- `id` (généré automatiquement)
- `title` (chaîne de caractères)
- `description` (chaîne de caractères)
- `status` (enum : 'TODO', 'IN_PROGRESS', 'DONE')

1.1. Créez un DTO pour la création d'une tâche.

1.2. Créez un contrôleur (`TasksController`) avec les routes suivantes :
   - GET `/tasks` - Récupérer la liste de toutes les tâches
   - GET `/tasks/:id` - Récupérer une tâche par ID
   - POST `/tasks` - Créer une nouvelle tâche
   - PUT `/tasks/:id` - Mettre à jour une tâche par ID
   - DELETE `/tasks/:id` - Supprimer une tâche par ID

1.3. Créez un service (`TasksService`) qui implémente les méthodes nécessaires pour interagir avec les tâches :
   - `getTaks()`
   - `getTaskById()`
   - `createTask()`
   - `updateTask()`
   - `deleteTask()`

1.4. Implémentez des contrôles de validation appropriés à l'aide des pipes NestJS pour garantir que les données d'entrée sont correctes.

1.5. Utilisez des `guards` pour protéger certaines routes, par exemple, pour s'assurer que seuls les utilisateurs authentifiés peuvent créer, mettre à jour ou supprimer des tâches.

1.6. **(Bonus)** Créez un `interceptor` qui logge les demandes HTTP entrantes.