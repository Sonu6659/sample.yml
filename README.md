version: v1.0
name: Hello World Playbook
agent:
  machine:
    type: e1-standard-2
    os_image: ubuntu1804

blocks:
  - name: Hello World
    task:
      env:
        VAR_NAME: "Hello, world!"
      jobs:
        - name: Print Hello World
          commands:
            - echo $VAR_NAME
