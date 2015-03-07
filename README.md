## vagrant-pyethereum

This launches a dev environment for `https://github.com/ethereum/pyethereum`

This is hardcoded to `192.168.33.22` so in order to be used in the ansible inventory file:

`config.vm.network :private_network, ip: "192.168.33.22"`
