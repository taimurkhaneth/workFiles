#!/bin/bash

# Create the .ssh directory if it doesn't exist
sudo mkdir -p /home/tanveer/.ssh

# Set the correct permissions for the .ssh directory
sudo chmod 700 /home/tanveer/.ssh

# Add the SSH public key to the authorized_keys file
echo "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQDPsq7fLVdTM1DErrtWkOSxcsg5iDDVu58rJ9p4xVJc3hq6gg997DnWKwtCqhtrodtf92B0rvWab7rDB49JXB5MxDEN1YajK7O5ftXCuz/cPLAl/CNyaHZcJcnJbX3GIO0J4sDt+uyFXqQVOXXZtCHPhEQbaPR3LNS5DEfUMIrUP6P9S8+fheu3pn3sNK5Ic1ovn4cCa0OTaFOhk5wQGttiIUo6J7cJwxxE3zHH6Qv6pomM+qMe/K9rbGue5QasJJzSxVkA8/09Oe6rv5wMKrDXVJdVDzXkSJCHf1aJ8Z6aN4SbE+d5tmVR/jBWXVdQCE/9qGbKhN1no4JJAllud6POsoj8yF0jhNlvPb1CxH1L5fMIdQEx6LiOK4IFW5F/Xk94+BSncRnG6/tR593Cy0fXQbz/AiHlmpC2jD1KgqIJrCNTzbOuRdMK4jjgwCzPIMunxz94b/x2LoPKuoKQL0Jx8j6E4+/lj5suqGjIROTtXcyV9dM6Zdpb7WJSv92IyXegNXVtKE3Ep9D9A0Cx4mEwxA3zR8y5x0rSvqkFMmpXjBmmk76x0h+2kSgeB2KebfJoL1bvYdBiGO2QBr2pyusYv+9+aYCINYxN6RgqzvZUu06M6BaYZqJXoAnHV13mVwSMxIpEuXUw26h2TRZlJF6/wu+pc4SYoor7wWnHxBdXaw==" | sudo tee /home/tanveer/.ssh/authorized_keys

# Set the correct permissions for the authorized_keys file
sudo chmod 600 /home/tanveer/.ssh/authorized_keys

# Set the ownership of the .ssh directory and authorized_keys file to the new user
sudo chown -R tanveer:tanveer /home/tanveer/.ssh
