![](./assets/header.png)

# CircleCI YAML Language Server

[![CircleCI](https://dl.circleci.com/status-badge/img/gh/CircleCI-Public/circleci-yaml-language-server/tree/master.svg?style=svg&circle-token=4f59ef1a4041930f4d07e37cb0b7ebd764f9689e)](https://dl.circleci.com/status-badge/redirect/gh/CircleCI-Public/circleci-yaml-language-server/tree/master)
[![GitHub release](https://img.shields.io/github/v/release/circleci-public/circleci-yaml-language-server)](https://github.com/circleci-public/circleci-yaml-language-server/releases)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](./LICENSE.md)

## This is CircleCI's YAML Language Server.
The official CircleCI extension for Visual Studio Code is available [on the VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=circleci.circleci). This extension was developed by the Developer Experience team of CircleCI and it includes two sets of features: the pipeline manager and the config helper. 

**The CircleCI config helper is based on a Language Server.** It provides language support for CircleCI YAML files. Thanks to the new VS Code extension, developers and DevOps engineers have access to direct feedback about the Config file they are editing, through features such as syntax validation and highlighting, rich navigation, on-hover documentation, autocompletion and usage hints.

In our case the Language Server is an implementation of the Language Server Protocol for CircleCI YAML config files that we have open sourced in order to provide more transparency to our community regarding the way the config helper works under the hood and by providing access for our community to take the language server capabilities to the IDE of their liking.

We believe that the CircleCI community is best placed to say what features are truly important or what bugs are the most annoying. We hope that the whole community will contribute to improving this tool by pointing out or addressing issues we might have overlooked. And we hope the value of this language server will be accessible to a great number of CircleCI users regardless of the IDE they choose to use.

The Language Server is implemented in Go 1.19+ and is, at its core, a JSON-RPC server that handles different calls (specified by the LSP spec). 

## Summary

- [Features](./README.md#features)
- [Platforms, Deployment and Package Managers](./README.md#platforms)
- [Contributing](./README.md#contributing)
- [Architecture Diagram](./README.md#architecture)
- [Code of Conduct](./CODE_OF_CONDUCT.md)  
- [Contribution Guidelines](./CONTRIBUTING.md)
- [Contributors](./README.md#contributor)
- [Quick Links](./README.md#quicklinks)
- [Credits](./README.md#credits)
- [Hacking](./HACKING.md)
- [License](./README.md#licence)

## <a name="features"></a>Features

<!-- Copied from circleci-vscode-extension/README.md, please keep sync! -->

This project provides in-file assistance to writing, editing and navigating
CircleCI Configuration files. It offers:

-   **Rich code navigation through “go-to-definition” and “go-to-reference”
    commands**. This is especially convenient when working on large
    configuration files, to verify the definition of custom jobs, executors
    parameters, or in turn view where any of them are referenced in the file.
    Assisted code navigation also works for Orbs, allowing to explore their
    definition directly in the IDE when using the go-to-definition feature on an
    orb-defined command or parameter.

<div style="text-align:center">
    <img src="https://images.ctfassets.net/il1yandlcjgk/knAhj4Gns5QidEb9ZQiwz/66bdeba70a7221bb12ad574e4f5e6572/config_helper_go-to-definition-optimised.gif" alt="circleci-vscode-go-to-definition" width="50%"/>
</div>

-   **Contextual documentation and usage hints when hovering on specific keys**,
    so to avoid you having to continuously switch to your browser to check the
    docs whenever you are editing your configuration. That said, links to the
    official CircleCI documentation are also provided on hover - for easier
    navigation.

<div style="text-align:center">
    <img src="https://images.ctfassets.net/il1yandlcjgk/3CFOeD8gH89Dq2A6P0aaGi/d2e2afdb3ec456df857533c413022c7c/config_helper_on-hover-documentation.png" alt="circleci-vscode-documentation-on-hover" width="50%"/>
</div>

-   **Syntax validation** - which makes it much easier to identify typos,
    incorrect use of parameters, incomplete definitions, wrong types, invalid or
    deprecated machine versions, etc.

<div style="text-align:center">
    <img src="https://images.ctfassets.net/il1yandlcjgk/6HXk81I7GxFwZ6F8X29CCN/a8b82d3f8a458c847ae9b1ac2e0b31f2/config_helper_syntax-validation.gif" alt="circleci-vscode-syntax-validation" width="50%"/>
</div>

-   **Usage warnings** - which can help identify deprecated parameters, unused
    jobs or executors, or missing keys that prevent you from taking advantage of
    CircleCI’s full capabilities

<div style="text-align:center">
    <img src="https://images.ctfassets.net/il1yandlcjgk/47wbq0Yp0BfIQMmVKg0vd2/86a6cf49af3c15848269b9f876b6b49e/config_helper_usage-warning.png" alt="circleci-vscode-usage-warnings" width="50%"/>
</div>

-   **Auto completion**, available both on built-in keys and parameters and on
    user-defined variables

<div style="text-align:center">
    <img src="https://images.ctfassets.net/il1yandlcjgk/lDNOHSw9R59F9nhhN3KWq/6adf764144b085e3d22c26de8e653a33/config_helper_autocomplete.png" alt="circleci-vscode-autocomplete" width="50%"/>
</div>

## <a name="platforms"></a>Platforms, Deployment and Package Managers

The tool is deployed through
[GitHub Releases](https://github.com/CircleCI-Public/circleci-yaml-language-server/releases).
Green builds on the `master` branch will publish a new GitHub release. These
releases contain binaries for macOS, Linux and Windows.

This is a project in active development, and we target a release frequency of one release per week on average. However, we reserve the right of releasing more or less frequently when necessary.

## <a name="contributing"></a>Contributing

Please feel free to contribute to this project, we update our Hall of fame - [CONTRIBUTORS.md](./CONTRIBUTORS.md) with all contributors who helped us fix a bug. You can find all the contribution guidelines and useful information in [CONTRIBUTING.md](./CONTRIBUTING.md). Development instructions for the CircleCI YAML Language Server can be found in [HACKING.md](HACKING.md).

## <a name="architecture"></a>Architecture diagram

![alt text](./assets/diagram.jpg)

## <a name="quicklinks"></a>Quick links

- [Install the VS Code extension using our language server](https://marketplace.visualstudio.com/items?itemName=circleci.circleci)

- [Discover how the language server was leveraged for the VS Code extension](https://youtu.be/Sdi7ctAXe2A)

- [Learn more about CircleCI](https://circleci.com/)

- [Do you have questions? Ask the circleCI community Discuss](https://discuss.circleci.com/)

## Social media links

<a href="https://twitter.com/intent/tweet?text=Take%20a%20look%20at%20the%20open%20sourced%20CircleCI%20Language%20Server%20on%20GitHub%20https%3A//github.com/CircleCI-Public/circleci-yaml-language-server%23readme%20via%20%40CircleCI" style="text-align:center; margin-right:15px">
    <img src="./assets/social/tw.png" alt="twitter-link" width="60px"/>
</a> 
<a href="https://www.facebook.com/sharer/sharer.php?u=https%3A//github.com/CircleCI-Public/circleci-yaml-language-server%23readme" style="text-align:center; margin-right:15px">
    <img src="./assets/social/fb.png" alt="facebook-link" width="60px"/>
</a> 
<a href="https://www.linkedin.com/shareArticle?mini=true&url=https%3A//github.com/CircleCI-Public/circleci-yaml-language-server%23readme" style="text-align:center">
    <img src="./assets/social/ln.png" alt="linkedin-link" width="60px"/>
</a> 

Help us get the word out! Share our project  
