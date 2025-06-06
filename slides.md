---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Localization in Enterprise Applications
  Using Contentful CMS for scalable content translation.
drawings:
  persist: false
css: unocss
---

# Internationalization in Enterprise

Scalable & Efficient Translation management


<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="avtar mt-36 rounded-full flex w-full align-center justify-center ">
  <img class="w-18 h-18 rounded-full grayscale" src="https://avatars.githubusercontent.com/u/6254009?v=4" />

  <a class="text-left ml-4 mt-2" href="https://github.com/sayjeyhi">
    <strong class="text-xl">Jafar Rezaei</strong> <br/>
    <span class="text-gray-400 text-sm">May 2025</span>
  </a>
</div>

---

# WHO AM I?
> Jafar Rezaei **@sayjeyhi**

<iframe class="mt-2" style="transform: scale(0.5, 0.5) translate(-50%, -50%); position: absolute; left: 10%; right: 50%; " src="https://sayjeyhi.com?v=2" width="160%" height="140%" />

---

# What is Internationalization?

<div class="flex items-center gap-4 justify-center mt-12">
<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExcHVjOTFyZWNoZWY5NnRxN2JkNmpoOGpkNmxpNm1oNTRjOW51N3F4dCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/3o7TKTDn976rzVgky4/giphy.gif" />
</div>

---

# What is Internationalization?

<div class="flex items-center gap-4 justify-center mt-12">
<ul class="text-left mr-12">
<li>en.json</li>
<li>fr.json</li>
<li>[...].json</li>
</ul>
<img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExY2J4N2xuZzljaHdva2E0cXdmeWQ3NWcwZWY1b29iM3BmMGd4bGUxeiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/VQ3ENfCBw7ljlvRo0u/giphy.gif" />
</div>

---

# What is Internationalization?

> Also known as **i18n**

**Definition:** The process of designing and developing a product, application, or website so that it can be easily adapted to different languages, regions, and cultures without requiring significant changes to the codebase.

**Key Focus:** Making the software flexible and adaptable for multiple <span v-mark="{ color: '#95a312', type: 'box' }">locales</span>.

**Examples:**

- Using Unicode to support multiple character sets.
- Separating translatable text from the code (e.g., using language files).
- Supporting right-to-left (RTL) and left-to-right (LTR) text layouts.
- Designing UI elements that can adjust based on text length and direction.

---

# Locales

> en-GB, fr-FR

Locale code is used to identify a specific language or region.
ISO standardized locale codes are a combination of a language code and a country code.


<div class="mt-12 grid grid-cols-2 border-t-1 border-dashed border-gray-500 p-t-2 text-base"> 
<span>


**Examples:**

- en-US <span class="text-gray-500">(English, United States)</span>
- fr-FR <span class="text-gray-500">(French, France)</span>
- be-NL <span class="text-gray-500">(Belgium, Netherlands)</span>
- be-FR <span class="text-gray-500">(Belgium, France)</span>


</span>

  <span>
<img src="/locale.png" class="w-64"/>
{LANGUAGE}-{COUNTRY}
</span>
</div>


---


# Other definitions as well!?
> G11N? L9N?

<br/> 

- Globalisation!
- Localization!

<div class="flex items-center gap-4 justify-center mt-8">
<img class="w-96" src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExbHl6cm41NXViN2c5c2Q2bDhrcGp0cnk1d2hwaHQwdTY1dHY0a3g5aSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/7vzGDZbRDSwS5axvZr/giphy.gif" />
</div>

---

# What is Localization?!

> Usually, localization is a process of adapting a product or service to a specific language or region.

<br />

<div class="scale-75">

|              | **Internationalization (i18n)**                       | **Localization (l10n)**                                     |
|--------------|-------------------------------------------------------|-------------------------------------------------------------|
| **Purpose**  | Prepares software for multiple languages and cultures | Adapts software for a specific language or region           |
| **Scope**    | Development phase (code-level implementation)         | Deployment phase (content and UI adaptation)                |
| **Involves** | Code structure, UI flexibility, encoding              | Translation, cultural adaptation, formatting                |
| **Example**  | Using placeholders for text ("Hello, {name}!")        | Replacing "Hello, {name}!" with "Hola, {name}!" for Spanish |

</div>

---


<div class="flex items-center gap-4 justify-center mt-12">
<img class="rounded-xl w-128" src="/What%20is%20Localization%20Image%201.jpeg" />
</div>

---


# Wider view

<div class="scale-95">

- **Globalization (g11n)**: The process of extending the reach of an organization's products beyond a <span v-mark.underline.orange>specific region</span>, language or culture, to deliver those products to a wider market.
- **Localization (l10n)**: adapting and customizing an internationalized product for <span v-mark.box.orange>one</span> or <span v-mark.box.orange>more target</span> markets. Localization takes into account language, culture, expectations, local standards and legal requirements, among other factors.

<br/>

- **Internationalization (i18n)**: accommodate different language conventions, date and time formats, and formatting instructions.
- **Translation (t9n)**: translating all readable text into the language of the target audience. This includes UI components, product labels, and supporting documentation.

</div>

---

# Let's make international project

<div class="flex items-center gap-4 justify-center mt-12">
<img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExYXIydm1tajZhYzlxb25wa3kydmM3ejU1d3lsbTdpd3M0bXFsMjllMiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/8PnbQkG5uCl0s/giphy.gif" />
</div>

---

# Decide on a locale
> How to decide on a locale code

<div class="text-yellow text-xl flex flex-col mt-10">
  https://www.sample.nl/en
</div>

**Country code**: <span class="text-yellow">NL</span>

**Language code**: <span class="text-yellow">??</span>

<div class="ml-4 grid grid-cols-2 border-b-1 border-dashed border-gray-300 p-2 text-base"> 
  <span class="text-gray-400">Query parameter: </span>
  <span class="text-yellow">en</span>
</div>
<div class="ml-4 grid grid-cols-2 border-b-1 border-dashed border-gray-300 p-2 text-base"> 
  <span class="text-gray-400">Cookie: </span>
  <span class="text-yellow">en</span>
</div>
<div class="ml-4 grid grid-cols-2 border-b-1 border-dashed border-gray-300 p-2 text-base"> 
  <span class="text-gray-400">Browser language: </span>
  <span class="text-yellow">nl</span>
</div>
<div class="ml-4 grid grid-cols-2 border-b-1 border-dashed border-gray-300 p-2 text-base"> 
  <span class="text-gray-400">TLD supported languages: </span>
  <span class="text-yellow">[nl, en]</span>
</div>
<div class="ml-4 grid grid-cols-2 p-2 text-base"> 
  <span class="text-gray-400">Fallback after all: </span>
  <span class="text-yellow">en</span>
</div>

---


# Simple i18n implementation

> having a language file per locale/domain and a default locale.

<br/>
<br/>

```mermaid {theme: 'dark' , scale: 1.4 }
graph LR
A(App) --> B(i18n)
B --> |Default| C[./locales/en.json]

B --> D[./locales/fr.json]
```

---

# Challenges of simple i18n

<br/>
<br/>

- No possibility to edit translations without changing the code
- Not the best experience for translators
- No dashboard to manage translations
- Hard to compare translations
- Needs manual translations
- Not possible to have screen shots of the translation keys

<br />

<div class="flex gap-2 text-sm items-center bg-gray-900 p-2 border-l-4 border-solid border-gray-300 rounded">
   <img class="w-6" src="https://em-content.zobj.net/source/microsoft-teams/363/winking-face_1f609.png" />
    It has advantages as as well, and it is still a valuable option to have for simple projects.
</div>

---

# Solutions

<div class="ml-4">

- tolgee
- localizejs
- lokalise
- contentful
- etc...

</div>

---

<div class="text-sm">

|                           | **Lokalise** 🏆                          | **Tolgee** 🔧                 | **Custom Contentful App** ⚙️                                 |  
|---------------------------|------------------------------------------|-------------------------------|--------------------------------------------------------------|  
| **Type**                  | SaaS Platform                            | Open-source & SaaS            | Fully Custom                                                 |  
| **CMS Integration**       | ✅ Yes (Contentful, GitHub, Figma)        | ✅ Yes (GitHub, Figma)         | ✅ Full control via API                                       |  
| **CMS Migrations**        | ❌ Limited                                | ❌ Limited                     | ✅ Fully controlled                                           |  
| **Automated Translation** | ✅ AI-based (Google, DeepL)               | ✅ AI-based (Google, DeepL)    | ✅ can have All integrations                                  |  
| **Collaboration**         | ✅ Role-based access, workflows           | ✅ Developer-friendly UI       | ✅ Customizable                                               |  
| **Self-Hosting**          | ❌ No                                     | ✅ Yes (Docker-based)          | ✅ Yes                                                        |  
| **Ease of Access**        | ✅ User-friendly UI                       | ✅ User-friendly UI            | ❌ Requires UI development                                    |  
| **Best For**              | Enterprises needing managed localization | Dev teams needing flexibility | Companies wanting full control & integration with Contentful |  

</div>

---

# Key Takeaways

- **Lokalise**: 
  - Best for enterprises needing <span v-mark="{ color: '#95a312', type: 'underline' }">scalable, managed localization</span> with a CMS.

- **Tolgee**: 
  - Great for <span v-mark="{ color: '#95a312', type: 'underline' }">developer-centric teams</span> wanting <span v-mark="{ color: '#95a312', type: 'underline' }">open-source/self-hosted</span> solutions.

- **Custom App with Contentful**: 
  - Ideal for teams needing <span v-mark="{ color: '#95a312', type: 'highlight' }">complete control over content workflows</span>, <span v-mark="{ color: '#95a312', type: 'highlight' }">seamless API integration</span>, and <span v-mark="{ color: '#95a312', type: 'highlight' }">flexibility in CMS migrations</span>.


---

# Contentful?

<div class="grid grid-cols-2 gap-4">

<div>


- **Headless CMS**
  - Flexible API-based content management
- **Multi-language support**
  - Built-in locale management
- **Integration possibilities**
  - Custom apps for automation
- **Scalability**
  - Suitable for enterprise-grade applications
- **SDK**
  - Contentful SDK for developers

</div>



<div class="ml-4">
<img src="https://images.ctfassets.net/jtqsy5pye0zd/54NhUPmKvUJ3tqIT7PS3uf/34ac8b293dbc40cb30ac13087b8de215/1200x630_with_logomark.png" class="h-70 w-auto rounded shadow" />
</div>

</div>


---

# Localization in Contentful

> For regular contents, Contentful provides a simple UI for managing content in multiple locales.

<div class="grid grid-cols-2 gap-4 pt-8">

<div>

<b>Step 1: Define Locales</b>


- In Contentful, go to **Settings → Locales**
- Add supported languages (e.g., English, French)
- Set a **default locale** (e.g., `en-US`)


</div>

<div>

<b>Step 2: Enable Field-Level Localization</b>

- In content models, enable **"Localization"**


</div>

</div>

<div v-click class="flex align-center justify-center mt-5">
  <img class="rounded-xl h-48" src="/cms-field-locales.png" />
</div>

---


# Implementing a custom Solution

<br/>

<div class="ml-4">
<div class="text-yellow text-2xl font-bold mb-2"> We wanted to have:</div>


<br/>

- ✅ Same DX as local development
- ✅ Full control over the translations
- ✅ Full control over the content workflows
- ✅ Seamless integration with Contentful
- ✅ A self-hosted solution
- ✅ Migrations possibility

</div>

---


# Translations

> Each translation is a key-value pair that maps a field to a value in a specific locale.


<div class="flex align-center justify-center mt-5">

```mermaid {theme: 'dark' , scale: 1.1 }
graph LR
A(key) --> B(value)

C(header.login.btn) --> |..Translates to..| D("Login")

```

</div>



```json
// en.json
{
    "header": {
        "login": {
            "btn": "Login"
        }
    }
}
```



---

# Migrations


<div class="flex align-center justify-center mt-12">

```mermaid {theme: 'default', scale: 0.8, 'themeVariables': {'git0': '#ff0000', 'git1': '#00ff00','git2': '#408af7','git3': '#ff00ff'}, 'gitGraph': {'showBranches': true, 'showCommitLabel':true} }
  gitGraph
    branch localhost/featenv
    commit id:"feature a"
    commit id:"feature b"
    commit id:"feature c"
    commit id:"feature d"
    commit id:"feature e"
    branch dev.site.com
    commit id:"Merge pr #34"
    commit id:"Merge pr #35"
    branch qual.site.com
    commit id:"Stable 1.2.0"
    commit id:"Stable 1.3.0"
    branch site.com
    checkout qual.site.com
    commit id:"Stable 1.4.0"
    commit id:"Stable 1.5.0"
    checkout site.com
    commit id:"Stable 1.2"
    commit id:"Stable 1.3"
    commit id:"hotfix 1.3.4"
    checkout dev.site.com
    commit id:"feature i"
    commit id:"feature j"
    commit id:"feature k"
    checkout localhost/featenv
    merge dev.site.com tag:"Current Master"
```

</div>

---

# Migrations



<div class="mt-8 flex gap-2 text-sm items-center bg-gray-900 p-2 border-l-4 border-solid border-gray-300 rounded">
   <img class="w-6" src="https://em-content.zobj.net/source/microsoft-teams/363/partying-face_1f973.png" />
    Contentful has also a <span v-mark.underline.orange>SDK API</span> for developers allows having migrations
</div>

<div class="flex align-center justify-center mt-12">

- Contentful has environments so we created (dev, qual, master)
- Mapped cms envs to git envs
- We had migration setup for cms
- Contents are live and editors can be editing them anytime.

</div>

<div v-click class="flex align-center justify-center mt-12">


```mermaid {theme: 'dark' , scale: 1.1 }
graph LR
A(local) --> | migration | B(dev) --> |migration| C(qual) --> |migration| D(master)


```

</div>

---

# Keys on contentful

<div class="ml-4 mt-12"> 

- has special content models to store keys
- supports types of keys
- supports screenshots of the keys
- allows adding descriptions

</div>

---

# Key Model

<img class="rounded-xl" src="/translation-key-type.png" />

---

# Key content

<img class="rounded-xl" src="/key-content.png" />

---

<span class="flex flex-col text-center center items-center justify-center h-full text-[30px]">

Automatically generate keys by comparing<br/><br/> dev files (`en.json`) with contentful keys
as part of 
   <div class="text-yellow-500 text-[70px] mt-12 font-extrabold ">Migrations!</div>

</span>


<div v-click class=" flex gap-2 text-sm items-center bg-gray-900 p-2 border-l-4 border-solid border-gray-300 rounded">
   <img class="w-6" src="https://em-content.zobj.net/source/microsoft-teams/363/partying-face_1f973.png" />
    We will use these migrations to migrate <strong>Values</strong> as well
</div>

---

<div class="flex flex-col text-center center items-center justify-center h-full text-[20px]">

- Now we have keys on our CMS 
- Migrated with changed
- We need to have a way to translate them.

</div>

---

# Building a Custom Translation App

What do we want to create?

<div class="-mt-12 flex flex-col text-center center items-center justify-center h-full text-[28px]">

A **UserInterface** to allow managing **Translation Values**.

</div>

---

# Building a Custom Translation App

<div class="grid grid-cols-2 gap-4">

<div>

<br/>

### **Why Use a Custom App?**

<br/>

- Provide seamless UI for editors
- Store translation history
- Improve accuracy by validating translations
- Support easier filtering of translations
- Support screen shots of the translation keys
- Allow import/export of translations


</div>

<div>

<br/>

### **Tech Stack**

<br/>

- Using contentful custom app starterkit
- f36 components
- react with contentful sdk

</div>

</div>

---


# Our current app

<img class="rounded-xl h-full w-auto" src="/app-config.png" />

---

# Our current app

<img class="rounded-xl h-full w-auto" src="/values.png" />

---

# GraphQL API

We use GraphQL to fetch the translations from the Contentful API.
```graphql
query {
  translationCollection(locale: "fr-FR") {
    items {
      ...keyValuePair
    }
  }
}
```

And combine it with graphql-codegen to generate the types and request functions.

```bash
npx graphql-codegen
```

<a href="https://github.com/dotansimha/graphql-code-generator" class="text-sm mt-6 inline-block">
https://github.com/dotansimha/graphql-code-generator
</a>


---

# Caching the translations

> We use Redis to cache the translations

<br/>
<br/>
<br/> 

- Redis is a key-value store
- We fetch the translations from the Contentful API
- Store the translations in Redis
- When the translations are requested, we fetch them from Redis

---

# Failure of APIs

> We have back-up of translation automatically created from CMS

<br/>
<br/>
<br/> 

- From time to time we copy translation content from CMS to git
- We can use these local files from the file-system if anything unexpected happens

---

<div class="flex align-center flex-col items-center mt-12">
<img class="w-32 mb-12" src="https://em-content.zobj.net/source/microsoft-teams/363/cowboy-hat-face_1f920.png" />

# Thank You!

<span class="text-xs -mt-4">

Slides: <a href="https://i18n.catshoulder.dev" class="text-blue-400">i18n.catshoulder.dev</a>

</span>

[GitHub](https://github.com/sayjeyhi) · [My Website](https://sayjeyhi.com)

</div>
