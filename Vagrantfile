Vagrant.configure("2") do |config|

    config.vm.box = "ubuntu/trusty64"

    config.vm.provider "virtualbox" do |v|
        v.memory = 1024
    end

    config.vm.define "wordpress" do |m|
        m.vm.network "private_network", ip: "{{wp_host_ip}}" ##set your wordpress private_network(delete this comment before running the project)
    end

    config.vm.define "mysql" do |m|
        m.vm.network "private_network", ip: "{{wp_db_ip}}" ##set your mysql private_network(delete this comment before running the project)
    end
end