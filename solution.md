# Documentation : Création d'une Unité d'Organisation, d'un Groupe d'Utilisateurs et d'un Utilisateur dans Active Directory

## Pré-requis
- Active Directory installé et configuré avec le domaine `wilders.lan`.
- Droits administratifs sur le serveur Active Directory.

## Étapes

### 1. Créer une Unité d'Organisation (OU) nommée `Wilders_students`

1. Ouvrez la console **Active Directory Users and Computers**.
2. Dans le volet de gauche, cliquez avec le bouton droit sur le domaine `wilders.lan` et sélectionnez **New** > **Organizational Unit**.
3. Nommez la nouvelle Unité d'Organisation `Wilders_students`.
4. Cliquez sur **OK** pour créer l'OU.

### 2. Créer un Groupe d'Utilisateurs nommé `Students`

1. Dans la console **Active Directory Users and Computers**, naviguez vers l'OU `Wilders_students` que vous venez de créer.
2. Cliquez avec le bouton droit sur `Wilders_students` et sélectionnez **New** > **Group**.
3. Nommez le groupe `Students`.
4. Choisissez le **Group scope** comme **Global** et le **Group type** comme **Security**.
5. Cliquez sur **OK** pour créer le groupe.

### 3. Créer un Utilisateur au sein du Groupe `Students`

1. Dans la console **Active Directory Users and Computers**, assurez-vous d'être dans l'OU `Wilders_students`.
2. Cliquez avec le bouton droit sur `Wilders_students` et sélectionnez **New** > **User**.
3. Remplissez les informations de l'utilisateur, par exemple :
   - **First name**: juda
   - **Last name**: brico
   - **User logon name**: judabrico
4. Cliquez sur **Next**.
5. Définissez un mot de passe pour l'utilisateur et configurez les options de mot de passe selon vos besoins.
6. Cliquez sur **Next**, puis sur **Finish** pour créer l'utilisateur.
7. Une fois l'utilisateur créé, faites un clic droit sur le nom de l'utilisateur (par exemple `John Doe`) et sélectionnez **Add to a group**.
8. Dans la fenêtre qui s'ouvre, tapez `Students` et cliquez sur **Check Names**. Si le groupe est trouvé, cliquez sur **OK** pour ajouter l'utilisateur au groupe `Students`.

## Conclusion

Vous avez maintenant créé une Unité d'Organisation `Wilders_students`, un Groupe d'Utilisateurs `Students`, et un utilisateur John Doe faisant partie de ce groupe sur votre domaine `wilders.lan`.

### Vérification

Pour vérifier que tout est configuré correctement :
- Ouvrez la console **Active Directory Users and Computers**.
- Naviguez vers l'OU `Wilders_students`.
- Assurez-vous que le groupe `Students` et l'utilisateur `juda brico` existent.
- Cliquez sur le groupe `Students` et vérifiez que `John Doe` est bien membre du groupe.

