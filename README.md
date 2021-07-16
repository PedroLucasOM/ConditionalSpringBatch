<h1 align="center" width="100vw">
  <img alt="Logo: ConditionalSpringBatch" src="https://github.com/PedroLucasOM/ConditionalSpringBatch/blob/master/logo.png" />
</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0-green.svg?cacheSeconds=2592000" />
  <img src="https://img.shields.io/badge/java-11-green.svg" />
  <img src="https://img.shields.io/badge/spring-2.5.2-green.svg" />
  <a href="https://github.com/PedroLucasOM/ConditionalSpringBatch#readme" target="_blank">
    <img alt="documentation" src="https://img.shields.io/badge/documentation-yes-green.svg" />
  </a>
  <a href="https://github.com/PedroLucasOM/ConditionalSpringBatch/graphs/commit-activity" target="_blank">
    <img alt="maintenance" src="https://img.shields.io/badge/maintained-yes-green.svg" />
  </a>
  <a href="https://twitter.com/PedroLucasOM" target="_blank">
    <img alt="Twitter: PedroLucasOM" src="https://img.shields.io/twitter/follow/PedroLucasOM.svg?style=social" />
  </a>
</p>

> :computer: Spring Batch Application to show like steps conditions :question: work.

# Topics

1. [About SpringBatch](https://github.com/PedroLucasOM/ConditionalSpringBatch#1-about-springbatch)
2. [About the Project](https://github.com/PedroLucasOM/ConditionalSpringBatch#2-about-the-project)
    - [Implemented Job](https://github.com/PedroLucasOM/ConditionalSpringBatch#implemented-job)
    - [Prerequisites](https://github.com/PedroLucasOM/ConditionalSpringBatch#prerequisites)
    - [Configuration](https://github.com/PedroLucasOM/ConditionalSpringBatch#configuration)
      - [Windows](https://github.com/PedroLucasOM/ConditionalSpringBatch#windows)
      - [Linux](https://github.com/PedroLucasOM/ConditionalSpringBatch#linux)
      - [Mac](https://github.com/PedroLucasOM/ConditionalSpringBatch#mac)
    - [Run](https://github.com/PedroLucasOM/ConditionalSpringBatch#run)
    - [Usage](https://github.com/PedroLucasOM/ConditionalSpringBatch#usage)
    - [Stop](https://github.com/PedroLucasOM/ConditionalSpringBatch#stop)
3. [Author](https://github.com/PedroLucasOM/ConditionalSpringBatch#3-author)
4. [Contributing](https://github.com/PedroLucasOM/ConditionalSpringBatch#4-contributing-)
5. [Show your support](https://github.com/PedroLucasOM/ConditionalSpringBatch#5-show-your-support)
6. [License](https://github.com/PedroLucasOM/ConditionalSpringBatch#6-license-)


# 1. About SpringBatch

It is a framework that uses the Java Virtual Machine and the Spring Ecosystem to build batch applications. By definition, batch systems are systems that realize a process of a finite amount of data without interaction or interruption.

To learn more about this framework, view this article on the Notion:
[SpringBatch Article](https://www.notion.so/Spring-Batch-4cc5c3c22b9b49c58f6c4e23097c3c9a)

# 2. About the Project

## Implemented Job

It is a simple job that executes 5 steps according to the output of each step execution and the passed parameter before the execution.

There are 5 steps:

- **conditionalStep1**
- **conditionalStep2**
- **conditionalStep3**
- **conditionalStep4**
- **conditionalStep5**

The application stats with the step **conditionalStep1**.

- If the ***FAIL*** parameter value is ***1***, the next step to be executed is **conditionalStep3**. 
- Otherwise, if the FAIL parameter value is ***2***, the next step to be executed is **conditionalStep4** and then **conditionalStep5**.
- If the FAIL parameter value isn't setted (parameter value = ***null***), the next step to be executed is **conditionalStep2**.

## Prerequisites

- docker

## Configuration

To run this application, you need to set an environment variable called ***FAIL_VALUE*** with the value of the error you want to see in execution. <br>
The possible values are: ***1***, ***2*** or ***empty***.

### Windows

In the Command Prompt, run:

``` sh
set FAIL_VALUE=
set FAIL_VALUE=1
set FAIL_VALUE=2
```

### Linux

In the terminal, run:

``` sh
export FAIL_VALUE=
export FAIL_VALUE=1
export FAIL_VALUE=2
```

### Mac

In the terminal, run:

```sh
touch ~/.bash_profile; open ~/.bash_profile
```

In TextEdit, add:

```sh
export FAIL_VALUE=
export FAIL_VALUE=1
export FAIL_VALUE=2
```

Save the .bash_profile file and Quit (Command + Q) Text Edit.

## Run

With the docker started, execute this command at the project root:

```sh
docker-compose up -d --build
```

## Usage

### Seeing the results in the log

In the base directory of the project with application running in the docker, run:

```sh
docker-compose logs -f -t app
```

You will see the executed job according to each FAIL_VALUE value.

## Stop

To stop correctly:

```sh
docker-compose down -v
```

Remember to execute this command each time that you want change the parameter value.

# 3. Author

👤 **Pedro Lucas**

* Twitter: [@PedroLucasOM](https://twitter.com/PedroLucasOM)
* Github: [@PedroLucasOM](https://github.com/PedroLucasOM)
* LinkedIn: [@PedroLucasOM](https://linkedin.com/in/PedroLucasOM)

# 4. Contributing 🤝

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/PedroLucasOM/ConditionalSpringBatch/issues).

# 5. Show your support

Give a :star: if this project helped you!

# 6. License 📝

Copyright © 2021 [Pedro Lucas](https://github.com/PedroLucasOM). <br />
