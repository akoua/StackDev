Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"
    config.vm.provider "docker" do |docker|
      docker.volumes = ["./:/app"]
      docker.build_dir = "."
      docker.ports = ["8085:8080"]
    end
    config.vm.provision "docker_compose", yml: "/vagrant/docker-compose.yml", run: "always"
  end
  