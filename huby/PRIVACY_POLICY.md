# Politique de confidentialité — Huby

**Dernière mise à jour :** 13 juillet 2026

## Résumé en une phrase

Huby lit vos notifications pour les afficher dans un flux unique sur votre téléphone. Aucune donnée ne quitte votre appareil.

---

## Quelles données Huby traite

### Contenu des notifications
Huby utilise l'API système Android `NotificationListenerService` pour capturer le contenu des notifications que vous recevez (titre, texte, application source, horodatage). Ces données sont nécessaires au fonctionnement principal de l'application : afficher un flux unifié de vos notifications.

### Contacts (optionnel)
Si vous activez l'option **"Associer les expéditeurs aux contacts"** dans les réglages, Huby lit vos contacts (`android.permission.READ_CONTACTS`) pour faire correspondre un numéro de téléphone ou une adresse email à un nom de contact. Cette fonctionnalité est **désactivée par défaut** et nécessite une action explicite de votre part.

Nous ne stockons **jamais** votre numéro de téléphone ou votre adresse email — uniquement le nom du contact résolu, à des fins d'affichage. Si vous désactivez cette option, les données associées sont supprimées immédiatement.

### Liste des applications installées
Huby utilise la permission `QUERY_ALL_PACKAGES` uniquement pour afficher le nom et l'icône corrects de l'application source d'une notification. Cette information n'est ni collectée, ni transmise — elle sert uniquement à l'affichage local.

---

## Où sont stockées vos données

**Exclusivement sur votre appareil.** Huby ne dispose d'aucun serveur, d'aucun compte utilisateur, et ne transmet aucune donnée sur Internet.

- Les notifications sont stockées dans une base de données locale (Room/SQLite)
- Vos préférences sont stockées localement (Android DataStore)
- La sauvegarde automatique Android (Google Backup) est **désactivée** pour Huby — vos données ne sont jamais copiées vers un service cloud

## Combien de temps vos données sont conservées

Vous contrôlez la durée de conservation dans les réglages de l'application : 7 jours, 30 jours, 90 jours, ou illimité. Passé ce délai, les notifications sont **supprimées automatiquement et définitivement** de l'appareil.

## Partage de données

Huby ne partage, ne vend, ni ne transmet aucune donnée à des tiers. Il n'y a :
- aucune publicité
- aucun outil d'analyse ou de tracking
- aucun SDK tiers de collecte de données
- aucune connexion réseau sortante liée à vos données personnelles

## Vos droits

Puisque toutes les données restent sur votre appareil :
- **Suppression** : désinstaller Huby supprime définitivement toutes les données associées
- **Contrôle** : vous pouvez désactiver la capture par application ou par canal de notification à tout moment dans les réglages
- **Accès** : vos données sont visibles directement dans l'application, aucune demande d'accès n'est nécessaire

## Permissions utilisées et pourquoi

| Permission | Usage |
|---|---|
| Accès aux notifications (`BIND_NOTIFICATION_LISTENER_SERVICE`) | Fonctionnalité principale — capturer les notifications |
| `QUERY_ALL_PACKAGES` | Afficher le nom/icône réel de l'application source |
| `READ_CONTACTS` (optionnel) | Associer un expéditeur à un contact, uniquement si activé |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Éviter que le système ne stoppe la capture en arrière-plan |

## Modifications de cette politique

Toute modification substantielle sera reflétée par une mise à jour de la date en haut de ce document.

## Contact

Pour toute question concernant cette politique de confidentialité : dev.q2ii@gmail.com
