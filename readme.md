

# Bruno Starter Guide

Bruno is an **open-source**, **Git-friendly**, **local-first** API client. This repository is the companion **Bruno Starter Guide** collection created by the Bruno team. It pairs with the official **[Quick Start](https://docs.usebruno.com/introduction/quick-start)** on the docs site and gives beginners a hands-on walkthrough inside the app.

You are welcome to go deeper anytime: topics like **authentication**, **scripting**, **proxy** settings, secrets, and CI help you get more out of the product—the Quick Start is only the beginning.

---

## What’s in this folder

After you [clone](https://github.com/bruno-collections/bruno-starter-guide) this repo or open it with **Fetch in Bruno**, you get an OpenCollection you can open in Bruno:


| Item                  | Purpose                                                                        |
| --------------------- | ------------------------------------------------------------------------------ |
| `opencollection.yml`  | Collection metadata (OpenCollection format)                                    |
| `*.yml` request files | Example and challenge requests (e.g. `github-api.yml`, `echo-bru.yml`)         |
| `environments/`       | Environment files such as `local.yml`                                          |
| `solutions.yaml`      | Reference solutions (optional to compare your work)                            |
| `submission/`         | **Where you place your exported OpenAPI file** after completing the challenges |


Open the **repository root** as the collection folder in Bruno so all requests and environments load correctly.

---

## The 12 challenges

Work through these **in order** (each step builds on the last). Full steps and screenshots live in the **[Quick Start guide](https://docs.usebruno.com/introduction/quick-start)**.

1. **Create a collection** — Name it **Bruno Starter Guide** (YAML recommended).
2. **Create a request** — e.g. GET `github-api` → `https://api.github.com/users/usebruno`.
3. **Send a request with data** — POST with JSON body (`echo-bru`).
4. **Create an environment** — e.g. `local` with variables like base URL.
5. **Write a test case** — Assertions on status or body.
6. **Write a script** — Pre-request or post-response script.
7. **Authentication** — Auth on a request (e.g. Bearer or as guided).
8. **Collection Runner** — Run multiple requests from the collection.
9. **API documentation** — Use collection/folder/request **Docs** where applicable.
10. **Git collaboration** — Commit/push or follow the Git workflow in the guide.
11. **Run a request through the CLI** — `bru run` from the collection directory.
12. **OpenAPI specifications** — Export the collection as OpenAPI from **Share → Export**.

---

## How to submit your challenge

1. Complete **all 12 challenges** above in your own Bruno collection (you can start from this repo or recreate it following the Quick Start).
2. In Bruno, export the collection to **OpenAPI** (see challenge 12 / Quick Start **OpenAPI** section).
3. Save the export as `**YourName.yaml`** (use your actual name in the filename, e.g. `jane-doe.yaml`).
4. Add that file to the `**submission/**` folder in this repository (you can look at `submission/usebruno.yaml` as an example of an exported spec).
5. Open a pull request or share the branch according to your course or team’s process.

If anything is unclear, use the [Quick Start](https://docs.usebruno.com/introduction/quick-start) as the source of truth for clicks, URLs, and success criteria.

---

## Fetch in Bruno

[Fetch in Bruno](https://fetch.usebruno.com?url=https%3A%2F%2Fgithub.com%2Fbruno-collections%2Fbruno-starter-guide.git)

---

## Links

- [Bruno downloads](https://www.usebruno.com/downloads)  
- [Documentation](https://docs.usebruno.com)  
- [Main Bruno repository](https://github.com/usebruno/bruno)

