# 🎓 Guia de Configuració: My-Eutic + Moodle

> **Temps estimat:** 15-20 minuts  
> **Requisits:** Accés d'administrador a Moodle  
> **Versions compatibles:** Moodle 3.8+, MoodleCloud

---

## 📋 Resum del Procés

```
1. Configurar My-Eutic com a eina externa a Moodle
2. Enviar el Client ID generat a l'equip My-Eutic
3. Crear una activitat LTI al teu curs
4. Provar l'accés
```

---

## Pas 1: Accedir a la Gestió d'Eines Externes

1. Inicia sessió a Moodle com a **Administrador**
2. Ves a: `Administració del lloc` → `Extensions` → `Mòduls d'activitat` → `Eina externa` → `Gestionar eines`

![Navegació a Gestionar eines](placeholder-nav-tools.png)

---

## Pas 2: Afegir My-Eutic (Mètode Automàtic ✨)

> **Recomanat** - Configura tot en 30 segons

1. Clica el botó **"Configuració a partir de l'URL de la cartutxeria"** (o "Configure a tool from a cartridge URL")

2. Enganxa aquesta URL:
   ```
   https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/lti/config
   ```

3. Clica **"Afegir LTI Advantage"**

4. Moodle carregarà automàticament tots els paràmetres

5. Clica **"Desa els canvis"**

![Configuració automàtica](placeholder-auto-config.png)

---

## Pas 2 (Alternatiu): Configuració Manual

Si el mètode automàtic no funciona, configura manualment:

1. Clica **"Configura una eina manualment"**

2. Omple els camps:

| Camp (Moodle Español) / (Català) | Valor a Introduir |
|------|-------|
| **Nombre de la herramienta** / Nom de l'eina | `My-Eutic Platform` |
| **URL de la herramienta** / URL de l'eina | `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/lti/launch` |
| **Versión LTI** / Versió LTI | `LTI 1.3` |
| **Tipo de clave pública** / Tipus de clau pública | `URL del conjunto de claves` / `URL del conjunt de claus` |
| **Conjunto de claves públicas** / Conjunt de claus | `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/jwks` |
| **Iniciar URL de inicio de sesión** / URL d'inici | `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/lti/login` |
| **URI(s) de redirección** / URI de redirecció | `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/lti/launch` |

3. A **"Ús de la configuració de l'eina"**, selecciona: `Mostra com a eina preconfigurada`

4. A **"Contenidor de llançament per defecte"**, selecciona: `Finestra nova` (recomanat)

5. Clica **"Desa els canvis"**

![Configuració manual](placeholder-manual-config.png)

---

## Pas 3: Obtenir el Client ID

Després de guardar, Moodle genera automàticament un **Client ID**.

1. A la llista d'eines, busca **"My-Eutic Platform"**
2. Clica la icona de **"Veure detalls de configuració"** (icona de llista)
3. Copia el **Client ID** (exemple: `r2pF0LJtV0kbY9K`)

![Obtenir Client ID](placeholder-client-id.png)

---

## Pas 4: Enviar Dades a My-Eutic

Envia un email a **suport@my-eutic.app** amb:

```
Assumpte: Configuració LTI - [Nom de la vostra escola]

- URL del Moodle: https://[la-teva-escola].moodlecloud.com
- Client ID: [el que has copiat]
- Nom de l'escola: [Nom complet]
- Email de contacte: [el teu email]
```

L'equip My-Eutic completarà la configuració en menys de 24h i et confirmarà per email.

---

## Pas 5: Crear una Activitat LTI al Curs

Un cop l'equip My-Eutic confirmi la configuració:

1. Ves a un **Curs** on vulguis afegir My-Eutic
2. Activa el **Mode d'edició**
3. Clica **"Afegeix una activitat o recurs"**
4. Selecciona **"Eina externa"**
5. A **"Eina preconfigurada"**, selecciona **"My-Eutic Platform"**
6. Posa un nom (ex: "Activitat d'Aprenentatge My-Eutic")
7. Clica **"Desa i mostra"**

![Afegir activitat](placeholder-add-activity.png)

---

## Pas 6: Provar l'Accés

1. Clica l'activitat que acabes de crear
2. Hauries de veure la pàgina de My-Eutic
3. Si ets professor, veuràs el Dashboard de Professor
4. Si ets estudiant, veuràs el Chat d'Aprenentatge

![Accés correcte](placeholder-success.png)

---

## ⚠️ Solució de Problemes

### "Error: Plataforma no configurada"

**Causa:** L'equip My-Eutic encara no ha completat la configuració.

**Solució:** Verifica que has enviat el Client ID i espera la confirmació.

---

### "Error: No s'ha pogut iniciar sessió"

**Causa:** L'usuari no existeix al curs de Moodle.

**Solució:** Assegura't que l'usuari està matriculat al curs.

---

### L'activitat s'obre en un iframe molt petit

**Causa:** Configuració de contenidor incorrecta.

**Solució:** Edita l'eina i canvia "Contenidor de llançament" a "Finestra nova".

---

## 📞 Suport

Si tens problemes, contacta:

- **Email:** suport@my-eutic.app
- **Horari:** Dilluns a Divendres, 9:00-18:00 (CET)

---

## Changelog

| Data | Canvis |
|------|--------|
| 2026-02-05 | Versió inicial de la guia pública |
