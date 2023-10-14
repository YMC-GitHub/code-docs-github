

- [x] add remote huggingface repo (webui)
```

```
[refer: repositories-getting-started ](https://huggingface.co/docs/hub/repositories-getting-started)



- [x] install huggingface-cli
```bash
python -m pip install huggingface_hub
```

- [x] login huggingface (cli)
```bash
huggingface-cli login
```

- [x] clone files from remote huggingface repo (https)
```bash
# git clone https://huggingface.co/<your-username>/<your-model-name>
```

- [x] Do you have files larger than 10MB ? 
```bash
git lfs install
```

- [x] if your files are larger than 5GB you’ll also need to run ?
```bash
huggingface-cli lfs-enable-largefiles .
```

- [x] push files to remote huggingface repo
```bash
git push
```

- [x] clone files from remote huggingface repo (ssh)
```bash
# git clone git@hf.co:<your-username>/<your-model-name>
```

- [x] Add a SSH key to your huggingface account (webui)

[refer: Add a SSH key to your huggingface account](https://huggingface.co/settings/keys)

- [x] Testing your SSH authentication
```bash
ssh -T git@hf.co
```

- [x] Adding a GPG key to your huggingface account (webui)

[refer: Add a GPG key to your huggingface account](https://huggingface.co/docs/hub/security-gpg)


- [x] Configure git to sign your commits with GPG
```bash
# git config user.signingkey <Your GPG Key ID>
# git config user.email <Your email on hf.co>
```

- [x]  add the -S flag to your git commit commands to sign your commits
```bash
git commit -S -m "My first signed commit"
```