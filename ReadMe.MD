# WIP

### Precondition

- Installing Golang v1.20.7
   - Download go1.20.7.linux-amd64.tar.gz from https://go.dev/dl/ 
   - ```sudo rm -rf /usr/local/go``` 
   - ```sudo tar -C /usr/local -xzf go1.20.7.linux-amd64.tar.gz```
   - ```export PATH=$PATH:/usr/local/go/bin```


### OpenTofu Installation (2*)

- ```git clone https://github.com/opentofu/opentofu.git```

- ```cd opentofu```

- ```go build -ldflags "-w -s -X 'github.com/opentofu/opentofu/version.dev=no'" -o bin/ ./cmd/tofu``` (3*)

- Then copy executable tofu file to your path, like: 

   - ```sudo cp ./bin/tofu /bin/```

- ```tofu version```

   - ```
        OpenTofu v1.6.0-beta1
        on linux_amd64
     ```

### Resources
1* https://github.com/opentofu/opentofu

2* [Install and use OpenTofu - Mathis Van Eetvelde](https://www.youtube.com/watch?v=a-lGAp9vWaQ)

3* https://github.com/opentofu/opentofu/blob/main/BUILDING.md