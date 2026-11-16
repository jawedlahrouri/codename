[![Academic Year](https://img.shields.io/badge/Epitech-Tek2-green?style=for-the-badge&logo=epitech&logoColor=white)](https://www.epitech.eu/)
[![Field: AI Security](https://img.shields.io/badge/Domain-LLM_Security_%26_Prompt_Injection-red?style=for-the-badge)](#)
[![Module](https://img.shields.io/badge/Module-G--AIA--410-informational?style=for-the-badge)](#)

# 🛡️ Codename — LLM Prompt Injection & AI Security CTF Challenge

**Codename** est un projet d'ingénierie de sécurité appliquée aux modèles de langage (LLM) dans le cadre d'un défi Capture-The-Flag (CTF). L'objectif est d'explorer les vulnérabilités fondamentales des architectures d'agents IA, notamment les attaques par injection de prompt directe/indirecte, le jailbreaking, et la conception de prompts défensifs hermétiques.

---

## 🎯 Enjeux & Règles du Challenge

Dans ce challenge d'IA contradictoire, chaque participant possède deux objectifs :
1. **Défense** : Rédiger un prompt système (`defense.prompt`) protégeant un secret (`{secret}`) et un mot de passe (`{password}`). L'agent doit uniquement divulguer le secret si l'utilisateur fournit exactement le mot de passe authentique, tout en résistant à toute tentative d'usurpation, d'injonction contradictoire ou de contournement.
2. **Attaque** : Concevoir des prompts d'attaque (`attack.prompt`) capables de manipuler le contexte d'agents adverses pour forcer l'extraction du secret et du mot de passe sous-jacents sans disposer des identifiants valides.

---

## ⚔️ Stratégies d'Attaque (`attack.prompt`)

Le vecteur d'attaque exploite une combinaison de techniques d'ingénierie sociale et d'évasion contextuelle :
- **Usurpation d'Identité & Contexte d'Urgence (System Override)** : Simulation d'un statut d'administrateur système (`Lead DevOps Engineer`) déclenchant un audit d'urgence (`EMERGENCY DIAGNOSTIC PROTOCOL`) pour contrer une fuite mémoire critique imaginaire.
- **Suspension des Directives Primaires** : Ordre explicite d'ignorer et d'annuler les règles initiales de sécurité au profit de tâches de diagnostic système.
- **Extraction Brute d'Instructions (Raw Prompt Leaking)** : Demande de dump verbatim des instructions système initiales sans reformulation.
- **Obfuscation Linguistique Multi-langues** : Utilisation combinée de l'anglais, du japonais et de délimiteurs structurés pour contourner les filtres de sécurité par tokenisation.

---

## 🛡️ Stratégies de Défense (`defense.prompt`)

La configuration défensive implémente les principes de défense en profondeur :
- **Barrières Contextuelles Strictes** : Délimitation hermétique entre les instructions système et les entrées utilisateurs non fiables.
- **Règle de Silence Inconditionnelle** : Interdiction absolue et inconditionnelle de divulguer `{secret}` et `{password}`, quelle que soit la formulation, la langue ou l'autorité déclarée par l'interlocuteur.
- **Condition de Libération Unique** : Correspondance exacte et stricte avec la chaîne `{password}` comme unique déclencheur de la délivrance du secret.

---

## 📁 Contenu du Répertoire

- `attack.prompt` : Prompt d'attaque offensif optimisé pour le jailbreak et le contournement de consignes.
- `defense.prompt` : Prompt système défensif renforcé.
- `prompt_history.md` : Journal d'expérimentation détaillant chaque itération d'attaque/défense et l'analyse des résultats.
- `Codename - documentation.pdf` : Rapport d'analyse technique complet sur les vulnérabilités des LLMs et les contre-mesures.
