# n8n-Data-flow
 How to process arrays and categorize people into "young" and "old" groups automatically.
 # dataflow-2nd flow

[![n8n](https://img.shields.io/badge/built%20with-n8n-3ebd70.svg)](https://n8n.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## Table of Contents

- [Project Overview](#project-overview)
- [Motivation](#motivation)
- [Features](#features)
- [Demo](#demo)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Author & Contact](#author--contact)
- [Acknowledgements](#acknowledgements)

---

## Project Overview

**dataflow-2nd flow**  
An n8n workflow that automatically categorizes users as "young people" or "old people" based on their age. It demonstrates looping, conditional branching, and data mapping in a no-code/low-code environment.

---

## Motivation

Segmenting user data and automating batch processing with clear, visual logic is a frequent business need. This project provides an easy-to-follow n8n workflow that saves time, reduces manual effort, and offers a reusable template for broader classification tasks.

---

## Features

- Manual workflow triggering for on-demand runs
- Array mapping and extraction via custom JavaScript
- Dynamic branching with conditional logic (age-based)
- Categorized outputs for "young" and "old" people, easily extendable

---

## Demo

![Workflow Screenshot](image.jpg)

**Sample run:**
- Users above age 40 are categorized as "old people"
- Users age 40 or below are categorized as "young people"
- Outputs show:  
  `They are old people`  
  `They are young people`  

---

## Prerequisites

- n8n instance (Cloud or Self-hosted)
- Node.js (for self-hosted n8n, v16.x+ recommended)
- Modern browser for n8n Editor

---

## Usage

1. In n8n Editor, open the imported "dataflow-2nd flow" workflow.
2. Review and (optionally) edit the array of users in the **Array** node:
3. 3. The **User Array** node converts the users into an itemized list.
4. The **If** node checks each user's `age`:
- If `age > 40`, sends user to **old people** node.
- Else, sends user to **Young people** node.
5. Run the workflow with the **Trigger Manual** node and review output at the bottom of the n8n UI.

---

## Configuration

- **To change the age threshold**:  
Edit the comparison in the **If** node (`age > 40`) to your desired logic.
- **To use your own data**:  
Modify the `users` array in the **Array** node.
- No special environment variables are required for this workflow.

---

## Roadmap

- [ ] Integrate external user sources (APIs, databases)
- [ ] Add email/SMS notification nodes for each category
- [ ] Make age threshold configurable via workflow input

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on submitting issues or pull requests.

---

## License

MIT

---

## Author & Contact

Maintained by Sharon
Email: jcsdigitech@gmail.com


---

## Acknowledgements

- The n8n team and documentation
- Inspiration from n8n workflow community




