# DeepManus Web UI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> Come From Open Source, Back to Open Source

**The default Web UI for [DeepManus](https://github.com/TimeCyber/DeepManus).**

DeepManus is a community-driven AI automation framework that builds upon the incredible work of the open source community. Our goal is to combine language models with specialized tools for tasks like web search, crawling, and Python code execution, while giving back to the community that made this possible.

## Demo

![demo](https://github.com/TimeCyber/DeepManus/blob/main/assets/demo.gif?raw=true)

- [View on YouTube](https://youtu.be/sZCHqrQBUGk)

## Table of Contents

- [Quick Start](#quick-start)
- [Docker](#docker)
- [Project Statement](#project-statement)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Quick Start

### Prerequisites

- [DeepManus](https://github.com/TimeCyber/DeepManus)
- Node.js (v22.14.0+)
- pnpm (v10.6.2+) as package manager

### Configuration

Create a `.env` file in the project root and configure the following environment variables:

- `NEXT_PUBLIC_API_URL`: The URL of the DeepManus API.

It's always a good idea to start with the given example file, and edit the `.env` file with your own values:

```bash
cp .env.example .env
```

### Installation

**IMPORTANT: First, **start the Python server**, see [DeepManus](https://github.com/TimeCyber/DeepManus) for more details.**

```bash
# Clone the repository
git clone https://github.com/TimeCyber/DeepManus-web.git
cd DeepManus-web

# Install dependencies
pnpm install

# Run the project in development mode
pnpm dev
```

Then open your browser and navigate to http://localhost:3000

Have fun!

## Docker

You can also run this project with Docker.

First, you need read the [configuration](#configuration) below. Make sure `.env` file is ready.

Second, to build a Docker image of your own web server:

```bash
docker build --build-arg NEXT_PUBLIC_API_URL=YOUR_DeepManus_API -t DeepManus-web .
```

Final, start up a docker container running the web server:

```bash
# Replace DeepManus-web-app with your preferred container name
docker run -d -t -p 3000:3000 --env-file .env --name DeepManus-web-app DeepManus-web

# stop the server
docker stop DeepManus-web-app
```

### Docker Compose

You can also setup this project with the docker compose:

```bash
# building docker image
docker compose build

# start the server
docker compose up
```

## Project Statement

This is an academically driven open-source project, developed by a group of former colleagues in our spare time. It aims to explore and exchange ideas in the fields of Multi-Agent and DeepResearch.

- **Purpose**: The primary purpose of this project is academic research, participation in the GAIA leaderboard, and the future publication of related papers.
- **Independence Statement**: This project is entirely independent and unrelated to our primary job responsibilities. It does not represent the views or positions of our employers or any organizations.
- **No Association**: This project has no association with Manus (whether it refers to a company, organization, or any other entity).
- **Clarification Statement**: We have not promoted this project on any social media platforms. Any inaccurate reports related to this project are not aligned with its academic spirit.
- **Contribution Management**: Issues and PRs will be addressed during our free time and may experience delays. We appreciate your understanding.
- **Disclaimer**: This project is open-sourced under the MIT License. Users assume all risks associated with its use. We disclaim any responsibility for any direct or indirect consequences arising from the use of this project.

## 项目声明

本项目是基于LangManus学术驱动的开源项目，修改了大模型引用Deepseek，去掉jina,更优化使用Playwright框架。旨在探索和交流 Multi-Agent 和 DeepResearch 相关领域的技术。

- **项目目的**：本项目的主要目的是大模型应用研究，给大模型装上手脚。
- **产权声明**：所属知识产权归成都时光赛博科技有限公司所有。
- **无关联声明**：本项目与 Manus（无论是公司、组织还是其他实体）无任何关联。
- **贡献管理**：Issue 和 PR 将在空闲时间处理，可能存在延迟，敬请谅解。
- **免责声明**：本项目基于 MIT 协议开源，使用者需自行承担使用风险。我们对因使用本项目产生的任何直接或间接后果不承担责任。

## Contributing

We welcome contributions of all kinds! Whether you're fixing a typo, improving documentation, or adding a new feature, your help is appreciated. Please see our [Contributing Guide](CONTRIBUTING.md) for details on how to get started.

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

Special thanks to all the open source projects and contributors that make DeepManus possible. We stand on the shoulders of giants.
