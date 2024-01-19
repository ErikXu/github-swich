# github-switch
A jenkins job to sync the fast github hosts

## How to Use

- Create a `Multibranch Pipeline` Job

- Add a `Git` Branch Sources

- Fill in the `Project Repository`

  <https://github.com/ErikXu/github-switch.git> for Github

  <https://gitee.com/erikxu/github-switch.git> for Gitee

- Set `Build Configuration`

  | Name | Value |
  | ------- | ------- |
  | Mode | by Jenkinsfile |
  | Script Path | Jenkinsfile |
