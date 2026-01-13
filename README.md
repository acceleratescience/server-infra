<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->

<!-- PROJECT SHIELDS -->
<!-- [![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![GPL License][license-shield]][license-url] -->
[![GPL License](https://img.shields.io/badge/License-GPLv3-brightgreen.svg)](https://opensource.org/licenses/)
[![Issues](https://img.shields.io/github/issues-raw/acceleratescience/server-infra.svg?maxAge=25000)](https://github.com/acceleratescience/server-infra/issues)
[![GitHub contributors](https://img.shields.io/github/contributors/acceleratescience/server-infra.svg?style=flat)]()
[![GitHub pull requests](https://img.shields.io/github/issues-pr/acceleratescience/server-infra.svg?style=flat)]()
[![PR's Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](http://makeapullrequest.com)
<br>
[![GitHub stars](https://img.shields.io/github/stars/acceleratescience/server-infra.svg?style=social&label=Star)]()
[![GitHub watchers](https://img.shields.io/github/watchers/acceleratescience/server-infra.svg?style=social&label=Watch)]()
[![GitHub forks](https://img.shields.io/github/forks/acceleratescience/server-infra.svg?style=social&label=Fork)](https://github.com/JonSnow/MyBadges)
[![GitHub followers](https://img.shields.io/github/followers/acceleratescience.svg?style=social&label=Follow)](https://github.com/JonSnow/MyBadges)
[![Twitter Follow](https://img.shields.io/twitter/follow/AccelerateSci.svg?style=social)](https://twitter.com/AccelerateSci)
<!-- [![LinkedIn][linkedin-shield]][linkedin-url] -->


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://acceleratescience.github.io/">
    <img src="./docs/assets/imgs/full_acc.png" alt="Logo" height=80>
  </a>

  <h3 align="center">Accelerate Science GPU Server Infrastructure</h3>

  <p align="justify">
    Infrastructure-as-code for deploying and managing GPU servers for machine learning research support.
  </p>
  <p align="center">
    <!-- <a href="https://acceleratescience.github.io/diffusion-models/" style="font-size: 20px; text-decoration: none"><strong>Start »</strong></a>
    <br />
    <br /> -->
    <a href="https://github.com/acceleratescience/large-language-models/issues">Report Bug</a>
    ·
    <a href="https://github.com/acceleratescience/large-language-models/issues">Request Feature</a>
    <br />
  </p>
</div>


<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#quick-start">Quick Start</a></li>
    <li><a href="#repository-structure">Repository Structure</a></li>
    <li><a href="#documentation">Documentation</a></li>
    <li><a href="#requirements">Requirements</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>



<!---------------------------------------------------------------------------->

[Button Shield]: https://img.shields.io/badge/Shield_Buttons-37a779?style=for-the-badge

[License]: LICENSE
[Shield]: Types/Shield.md
[#]: #


<!---------------------------------[ Badges ]---------------------------------->

[Badge License]: https://img.shields.io/badge/-BY_SA_4.0-ae6c18.svg?style=for-the-badge&labelColor=EF9421&logoColor=white&logo=CreativeCommons
[Badge Likes]: https://img.shields.io/github/stars/MarkedDown/Buttons?style=for-the-badge&labelColor=d0ab23&color=b0901e&logoColor=white&logo=Trustpilot


This repository contains the configuration, deployment scripts, and documentation for running:

- **LLM inference services** (vLLM + LiteLLM proxy)
- **Monitoring stack** (Prometheus + Grafana + DCGM exporter)
- **Workshop environments** (JupyterHub for training sessions)

## Quick Start

1. Clone this repository
2. Copy example files and configure for your environment:
```bash
   cp ansible/inventory.ini.example ansible/inventory.ini
   # Edit inventory.ini with your server details
```
3. Run the bootstrap playbook to set up the base system:
```bash
   ansible-playbook -i ansible/inventory.ini ansible/playbooks/setup.yml
```
4. Deploy the monitoring stack:
```bash
   ansible-playbook -i ansible/inventory.ini ansible/playbooks/monitoring.yml
```

## Repository Structure
```
ansible/          # Ansible playbooks for server configuration
docs/             # Documentation and Architecture Decision Records
scripts/          # Operational scripts (mode switching, maintenance)
stacks/           # Docker Compose definitions for each service
```

## Documentation

- [Getting Started](docs/getting-started.md) - Detailed setup instructions
- [System Architecture](docs/system.md) - How the components fit together
- [ADRs](docs/ADRs/) - Architecture Decision Records explaining key choices

## Requirements

- Ubuntu 22.04 LTS (server)
- NVIDIA GPU with recent drivers
- Docker and Docker Compose
- Ansible (on your local machine, for deployment)

## License

GNU GPLv3 - See [LICENSE](LICENSE) for details.

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/acceleratescience/server-infra.svg?style=for-the-badge
[contributors-url]: https://github.com/acceleratescience/server-infra/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/acceleratescience/server-infra.svg?style=for-the-badge
[forks-url]: https://github.com/acceleratescience/server-infra/network/members
[stars-shield]: https://img.shields.io/github/stars/acceleratescience/server-infra.svg?style=for-the-badge
[stars-url]: https://github.com/acceleratescience/server-infra/stargazers
[issues-shield]: https://img.shields.io/github/issues/acceleratescience/server-infra.svg?style=for-the-badge
[issues-url]: https://github.com/acceleratescience/server-infra/issues
[license-shield]: https://img.shields.io/github/license/acceleratescience/server-infra.svg?style=for-the-badge
[license-url]: https://github.com/acceleratescience/server-infra/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/company/accelerate-programme-for-scientific-discovery/
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 