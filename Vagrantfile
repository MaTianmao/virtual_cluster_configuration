Vagrant.configure(2) do |config|
  # 如果需要三台就(1..3)的形式
  (1..3).each do |i|
    config.vm.define "vm#{i}" do |node|
      node.vm.box = "glusterfs"
      node.vm.hostname = "vm#{i}"
      node.vm.network "private_network", ip: "192.168.111.10#{i}"
      # 映射目录 根据自己实际情况配置
      node.vm.provider "virtualbox" do |v|
        v.name = "fs#{i}"
        v.memory = 2048
		v.cpus = 1
      end
	  
    end
  end
end
