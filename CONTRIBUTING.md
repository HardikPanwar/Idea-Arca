# Contributing

Here are some ways you can contribute to this project:

- Add Themes
- Add Ideas
- Report/Fix bugs.
- Write documentation.
- Others : Implement New Features , Modify UI/UX

---

# Contributions

The Different Types of Contribution are explained below :

## ADD Themes

Here we are talking about the theme for the website.
The process to add theme is (After Fork And Clone):</br>
we are showing an eg by adding a theme called `test`.

1. Add a new `<option>` in `./src/components/Header.astro` :

- Before

```js
<select name="themes" id="themes" class="btn">
  /* other options */
  <option value="neon">Neon</option>
</select>
```

- After

```js
<select name="themes" id="themes" class="btn">
  /* other options */
  <option value="neon">Neon</option>
  /* Added code 👇 */
  <option value="test">Test</option>
</select>
```

2. Adding a new `class` code in `./src/styles/global.scss` :

- Before

```scss
/* Other Codes*/
.neon {
  --primary-1: #793fdf;
  --primary-2: #7091f5;
  --primary-3: #97fff4;
  --primary-4: #ffffff;
  --sidenav: #793fdfce;
  --gradient: #e600ff;
}
```

- After

```scss
/* Other Codes*/
.neon {
  /*same*/
}
/* Added code 👇 */
.test {
  --primary-1: #000000;
  --primary-2: #000132;
  --primary-3: #000245;
  --primary-4: #ffffff;
  --sidenav: #0000ce;
  --gradient: #f690fa;
}
```

### NOTE :

1. `--primary-1` : is used as the main background
2. `--primary-3` : is mostly used my important texts
3. `--primary-4` : is used by detailed texts
4. `--sidenav` : is reduced opacity of `--primary-1`, just append `ce` of your `--primary-1`;
5. `--gradient` : this is a `random color` which suits the website, it's the color of the gradient circle at top of the website

_**You can use https://colorhunt.co/ for the 4 Primary Colors, and choose a nice color for gradient on your own**_



## ADD Ideas

Here we are talking about the ideas displayed on the website.
The process to add ideas is (After Fork And Clone):</br>

### **CASE 1** : Adding Idea in Existing Section/Field

we are showing an example by adding an idea in `React` section.

1. Add Your Object in the `./src/database/MainData.json` inside the `data` of React section :

- Before

```js
[
  {
    section: "React",
    data: [
      {
        id: 1,
        title: "E-commerce Dashboard",
        tags: ["React", "Redux", "CSS", "API Integration"],
        description: "Lorem Ispum",
        link: "https://example-ecommerce-dashboard.com",
      },
    ],
  },
];
```

- After

```js
[
  {
    section: "React",
    data: [
      {
        // prev code
      },
      /* Added code 👇 */
      {
        id: 2,
        title: "Test",
        tags: ["React", "Redux", "scss", "API"],
        description: "Give Meaningful Description, there is no word limit",
        link: "Working Link",
      },
    ],
  },
];
```

### **CASE 2** : Adding Idea in a New Section/Field

we are showing an example by adding an idea in a new sectio : `BackboneJs` section.

1. Add Your Section Name in `./src/database/sections.json`, to make your section/field appear in left navigation panel :

- Before

```js
["React", "Vue", "Svelte", "Frontend", "Backend"];
```

- After

```js
["React", "Vue", "Svelte", "Frontend", "Backend", "BackboneJs"];
```

2. Add Your Object in the `./src/database/MainData.json` inside the `data` of React section :

- Before

```js
[
  {
    section: "React",
    data: [
      {
        id: 1,
        title: "E-commerce Dashboard",
        tags: ["React", "Redux", "CSS", "API Integration"],
        description: "Lorem Ispum",
        link: "Working Link",
      },
    ],
  },
  // Similar Codes for Other Sections
];
```

- After

```js
[
  // prev Codes
  {
    section: "BackboneJs",
    data: [
      {
        id: 1,
        title: "E-commerce Dashboard",
        tags: ["Backbonejs"],
        description: "Give Meaningful Description, there is no word limit",
        link: "Working Link",
      },
    ],
  },
];
```

### NOTE :

1. `section` : the major Fields
2. **`link` : It should be a working, non-broken link. It can be a figma, hosted website link. If your idea is based on any other already existing website (can be desings or any feature), then provide that website link.**
3. *All the `id` in each sections must be **unique***
