# TERRAFORM ANYWHERE

You may have found that sometimes moving across different cpu architectures in terraform is not as easy as it should be. This tool will help you to use any version of terraform no matter what architecture your cpu has. The best part is that you don't need to install anything else than docker.

## INSTALLATION

1- Execute following command to use the last version of this tool.

```bash
curl https://raw.githubusercontent.com/gerardVM/terraform-anywhere/main/terraform-anywhere.sh > ~/.terraform-anywhere
```

2- Include an extra line to your ~/.bashrc file to source your new configuration.
```bash
echo "[ \$(echo \$(which docker)) ] && . ~/.terraform-anywhere" >> ~/.bashrc
```

Once these commands are executed, open a new terminal and then you are good to go.

Be aware that you may have limitations if you are trying to perform complex operations. Toolset is: make, mlocate, bash, openssh-client, git, jq and yq

## HOW TO USE IT

You just need to set the version you want by setting the variable TF_VERSION.

In order to track versions, a .tf_\<version>-alpine file will be created in each directory you use this tool.

You need to be aware that both "terraform" and "make" commands are being redirected to the docker container.

## HOW TO STOP USING IT

If you want to stop using this tool, just remove or comment the line you added to your ~/.bashrc file and remove the ~/.terraform-anywhere file.

## Contributing

Pull requests are welcome

## License

[MIT](LICENSE)
