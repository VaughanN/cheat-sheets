
```
sudo apt install libayatana-appindicator3-1
```

```
sudo apt install libappindicator3-1
```

-- Copy the downloaded NSClient_\<key\>.run to the distro and make it executable.

```
sudo chmod 777 NSClient_addon-itdynamics.goskope.com_20542_ycmjuRbbFnf73ZW8kDkN_72pdOOf9L0FB2HqplfaK9qn9hvdHxkbKcl03o42_.run
```

```
sudo ./NSClient_addon-itdynamics.goskope.com_20542_ycmjuRbbFnf73ZW8kDkN_72pdOOf9L0FB2HqplfaK9qn9hvdHxkbKcl03o42_.run
```

```
systemctl status stagentd.service
```



-- Copy Ubuntu /usr/local/share/ca-certificates to other distros ~./downloads/
```
sudo mv downloads/ca-certificates/ /usr/local/share
```

-- Alma
```
sudo ln -s /usr/local/share/ca-certificates/nscacert.crt /etc/pki/ca-trust/source/anchors/nscacert.pem  && sudo ln -s /usr/local/share/ca-certificates/nstenantcert.crt  /etc/pki/ca-trust/source/anchors/nstenantcert.pem
```

-- Arch
```
sudo trust anchor --store /usr/local/share/ca-certificates/nscacert.crt && sudo trust anchor --store /usr/local/share/ca-certificates/nstenantcert.crt
```
