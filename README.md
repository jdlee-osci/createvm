# Create VM

git clone

```Shell Session
git clone https://github.com/jdlee-osci/createvm.git
cd createvm
```

샘플 ansible-hosts 파일 복사 후 수정  
kvm_server 는 libvirtd 가 설치 된 서버 설정 local 서버 설정도 가능  
vms 세션에 생성할 vm 들 정보를 입력  

```Shell Session
cp sample/ansible-hosts .
vi ansible-hosts
```

group_vars/all.yml 내용을 필요한 경우 수정  
ansible-playbook 실행

```Shell Session
cp group_vars/all.yml.sample group_vars/all.yml
vi group_vars/all.yml

ansible-playbook main.yml
```

기본적으로 같은 이름의 기존 vm 을 삭제하고 진행하니 이 부분에 주의

