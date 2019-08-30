---
description: Comment réparer votre partition Linux devenu inutilisable
---

# Partition endommagé

{% hint style="info" %}
Si votre pc démare bien mais que vous démarez en `Recovery Mode`
{% endhint %}

1. Vérifiér que vous sortez du Recovey en tapant : `sudo mount`
2. Utilisez l'outil de réparation : `sudo fslk /home` puis répondez yes aux questions
3. Au prochain démmarage vous devriez bootez correctement !

