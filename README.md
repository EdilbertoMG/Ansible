# Iniciar Ansible Instalar
 pip install ansible

# Crear Dockers
docker build -t server:16.04 .

# Crear Maquinas 
../create_dockers.sh server:16.04

# Configuracion Alias
echo "127.0.0.1 server01 server02 server03" | sudo tee -a /etc/hosts

# Permisos
chmod 0600 key*

# Actualizar Llaves
../clean_all.sh

# Iniciar los Playbook
ansible-playbook -i ../hosts inicial.yml

ansible-playbook -i ../hosts inicial.yml

