---
description: Comment réparer votre partition Linux devenu inutilisable
---

# Partition endommagée

{% hint style="info" %}
Ces instruction sont à suivre si votre session Linux ne démarre pas correctement et que vous démarrez en **Recovery Mode** 
{% endhint %}

1. Vérifier que vous sortez du Recovery en tapant : `sudo mount`
2. Utilisez l'outil de réparation : `sudo fslk /home` puis répondez yes aux questions
3. Au prochain démarrage vous devriez bootez correctement !



