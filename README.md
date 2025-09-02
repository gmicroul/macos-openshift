# macos-openshift
macos-openshift testing

#1, download and install crc
wget https://developers.redhat.com/content-gateway/file/pub/openshift-v4/clients/crc/2.53.0/crc-macos-installer.pkg
double click the pkg file to install,next,next...finish.
#2, start crc daemon
crc daemon start
INFO listening /Users/xxx/.crc/crc-http.sock  
INFO listening /Users/xxx/.crc/tap.sock       
INFO listening on /Users/xxx/.crc/crc-unixgram.sock 
 - - [02/Sep/2025:22:53:49 +0800] "GET /api/version HTTP/1.1" 200 101
 - - [03/Sep/2025:01:48:25 +0800] "GET /api/version HTTP/1.1" 200 101
#3，setup crc
crc setup
INFO Using bundle path /Users/xxx/.crc/cache/crc_vfkit_4.19.3_arm64.crcbundle 
INFO Checking if running macOS version >= 13.x    
INFO Checking if running as non-root              
INFO Checking if crc-admin-helper executable is cached 
INFO Checking if running on a supported CPU architecture 
INFO Checking if crc executable symlink exists    
INFO Checking minimum RAM requirements            
INFO Check if Podman binary exists in: /Users/xxx/.crc/bin/oc 
INFO Checking if running emulated on Apple silicon 
INFO Checking if vfkit is installed               
INFO Checking if CRC bundle is extracted in '$HOME/.crc' 
INFO Checking if /Users/xxx/.crc/cache/crc_vfkit_4.19.3_arm64.crcbundle exists 
INFO Getting bundle for the CRC executable        
INFO Downloading bundle: /Users/xxx/.crc/cache/crc_vfkit_4.19.3_arm64.crcbundle... 
5.74 GiB / 5.74 GiB [-------------------------------------------------------------------------------] 100.00% 7.62 MiB/s
INFO Uncompressing /Users/xxx/.crc/cache/crc_vfkit_4.19.3_arm64.crcbundle 
crc.img:  31.00 GiB / 31.00 GiB [------------------------------------------------------------------------------] 100.00%
oc:  138.85 MiB / 138.85 MiB [---------------------------------------------------------------------------------] 100.00%
INFO Checking if old launchd config for tray and/or daemon exists 
INFO Checking if crc daemon plist file is present and loaded 
INFO Adding crc daemon plist file and loading it  
INFO Checking SSH port availability               
Your system is correctly setup for using CRC. Use 'crc start' to start the instance

#4，start crc
crc start
crc start       
INFO Using bundle path /Users/xxx/.crc/cache/crc_vfkit_4.19.3_arm64.crcbundle 
INFO Checking if running macOS version >= 13.x    
INFO Checking if running as non-root              
INFO Checking if crc-admin-helper executable is cached 
INFO Checking if running on a supported CPU architecture 
INFO Checking if crc executable symlink exists    
INFO Checking minimum RAM requirements            
INFO Check if Podman binary exists in: /Users/xxx/.crc/bin/oc 
INFO Checking if running emulated on Apple silicon 
INFO Checking if vfkit is installed               
INFO Checking if old launchd config for tray and/or daemon exists 
INFO Checking if crc daemon plist file is present and loaded 
INFO Checking SSH port availability               
INFO Loading bundle: crc_vfkit_4.19.3_arm64...    
CRC requires a pull secret to download content from Red Hat.
You can copy it from the Pull Secret section of https://console.redhat.com/openshift/create/local.
? Please enter the pull secret 
X Sorry, your reply was invalid: empty pull secret
X Sorry, your reply was invalid: empty pull secret
? Please enter the pull secret *****************************************************************************************
INFO Creating CRC VM for OpenShift 4.19.3...      
INFO Generating new SSH key pair...               
INFO Generating new password for the kubeadmin user 
INFO Starting CRC VM for openshift 4.19.3...      
INFO CRC instance is running with IP 127.0.0.1    
INFO CRC VM is running                            
INFO Updating authorized keys...                  
INFO Configuring shared directories               
INFO Check internal and public DNS query...       
INFO Check DNS query from host...                 
INFO Verifying validity of the kubelet certificates... 
INFO Starting kubelet service                     
INFO Waiting for kube-apiserver availability... [takes around 2min] 
INFO Adding proxy configuration to the cluster... 
INFO Adding user's pull secret to the cluster...  
INFO Updating SSH key to machine config resource... 
INFO Waiting until the user's pull secret is written to the instance disk... 
INFO Overriding password for developer user       
INFO Changing the password for the users          
INFO Updating cluster ID...                       
INFO Updating root CA cert to admin-kubeconfig-client-ca configmap... 
INFO Starting openshift instance... [waiting for the cluster to stabilize] 
INFO 8 operators are progressing: console, image-registry, ingress, kube-apiserver, kube-controller-manager, ... 
INFO 9 operators are progressing: console, image-registry, ingress, kube-apiserver, kube-controller-manager, ... 
INFO 9 operators are progressing: console, image-registry, ingress, kube-apiserver, kube-controller-manager, ... 
INFO 9 operators are progressing: console, image-registry, ingress, kube-apiserver, kube-controller-manager, ... 
INFO 9 operators are progressing: console, image-registry, ingress, kube-apiserver, kube-controller-manager, ... 
INFO 9 operators are progressing: console, image-registry, ingress, kube-apiserver, kube-controller-manager, ... 
INFO 9 operators are progressing: console, image-registry, ingress, kube-apiserver, kube-controller-manager, ... 
INFO 8 operators are progressing: console, image-registry, kube-apiserver, kube-controller-manager, kube-storage-version-migrator, ... 
INFO 8 operators are progressing: console, image-registry, kube-apiserver, kube-controller-manager, kube-storage-version-migrator, ... 
INFO 8 operators are progressing: console, image-registry, kube-apiserver, kube-controller-manager, kube-storage-version-migrator, ... 
INFO 8 operators are progressing: console, image-registry, kube-apiserver, kube-controller-manager, kube-storage-version-migrator, ... 
INFO 8 operators are progressing: console, image-registry, kube-apiserver, kube-controller-manager, kube-storage-version-migrator, ... 
INFO 8 operators are progressing: console, image-registry, kube-apiserver, kube-controller-manager, kube-storage-version-migrator, ... 
INFO 8 operators are progressing: console, image-registry, kube-apiserver, kube-controller-manager, kube-storage-version-migrator, ... 
INFO 5 operators are progressing: console, image-registry, kube-apiserver, kube-storage-version-migrator, openshift-controller-manager 
INFO 3 operators are progressing: authentication, console, kube-apiserver 
INFO Operator console is progressing              
INFO Operator console is progressing              
INFO Operator console is progressing              
INFO All operators are available. Ensuring stability... 
INFO Operators are stable (2/3)...                
INFO Operators are stable (3/3)...                
INFO Waiting for the proxy configuration to be applied... 
INFO Adding crc-admin and crc-developer contexts to kubeconfig... 
Started the OpenShift cluster.

The server is accessible via web console at:
  https://console-openshift-console.apps-crc.testing

Log in as administrator:
  Username: kubeadmin
  Password: xxx-xxx-xxx-xxx

Log in as user:
  Username: developer
  Password: xxxxxx

Use the 'oc' command line interface:
  $ eval $(crc oc-env)
  $ oc login -u developer https://api.crc.testing:6443

oc version
Client Version: 4.19.3
Kustomize Version: v5.5.0
Kubernetes Version: v1.32.5

