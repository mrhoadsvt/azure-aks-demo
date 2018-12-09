# Configuring Secret via kubectl
In order to configure the secret "azureregistrykey", run the following command.  Running this on Ubuntu 18.04, I was unable to authentication using other methods.

    kubectl create secret docker-registry azureregistrykey \
    --docker-server=<your registry>.azurecr.io --docker-username=<your username> \
    --docker-password=<your password> --docker-email=<youremail address>
  
Then ensure that imagePullSecrets matches "azureregistrykey" or whatever you've called it.
