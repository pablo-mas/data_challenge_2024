### **Métrique**
La métrique utilisée est le **score F1 en micro-moyenne**, une métrique de performance utilisée dans les tâches de classification multi-étiquettes. Elle combine la précision et le rappel en une seule métrique qui prend en compte le déséquilibre des classes. Voici son fonctionnement :

- ***Précision*** : Le rapport entre les prédictions positives correctes (vrais positifs) et le nombre total de prédictions positives faites (vrais positifs + faux positifs).
- ***Rappel*** : Le rapport entre les prédictions positives correctes (vrais positifs) et le nombre total d'instances positives réelles (vrais positifs + faux négatifs).
- ***Score F1*** : La moyenne harmonique de la précision et du rappel, qui équilibre ces deux métriques.

**Micro-moyenne :** <br>
Lorsqu'on traite plusieurs classes ou étiquettes, la micro-moyenne calcule la métrique en additionnant les vrais positifs, les faux positifs et les faux négatifs **à travers toutes les classes**, puis en calculant la précision et le rappel à partir de ces totaux agrégés.


<div style="text-align: center;">
    <img src="https://i.ibb.co/Pxrw6Q5/Picture3.png" alt="Alt text" width="400" height="200">
</div>


### **Référence**
Un score de référence a été obtenu en convertissant les SMILES en empreintes de Morgan, puis en entraînant un algorithme de l'arbre de décision avec les paramètres par défaut de scikit-learn. Vous pouvez reproduire ce score en utilisant le carnet d'introduction associé au défi.
