git init   :   ���� ���͸��� Ȩ���� ����..?

�������� �����
vim f1.txt : �ؽ�Ʈ ����� ���� ���� vi����

git status : ���� ���� ���� Ȯ��

git add f1.txt : ���� ���� ���� = commit ��� ���·� ����
�ٽ� git status   �ϸ� new file �̸��� ����

�� �̸� �ο�

git config --global user.name stairs
git config --global user.mail sungdoolim@naver.com
git commit

git log   �ϸ� ������ ����
git log -p   : ������ ���

���� :
vim f1.txt �ؼ� ���� ���� ������ 
git status �ϸ� modified�� ��� ������
���� git add f1.txt�������
���Ŀ� git status�ϸ� modifeid �����
���� git commit�� ���� ���ֱ� 2???

git log  [commit �ּ�]
�� ���� �������� �αװ� ����
git diff [Ŀ���ּ�]..[Ŀ���ּ�]
 : ���� ���

���� ���� ������
git diff �ϸ� ���� ���ϰ��� ���� �� ������
add �ϰ��Ŀ��� �Ⱥ�����


���� �������� ���ư���
 
git reset [���ϴ� ������ Ŀ�� �ּ�] --hard
�ϸ� �� Ŀ�� �ּ� ������ ������ ����


���� ���������� add �ϰ� commit �ϱ� ����

git commit --help �� ���� ����

��� : vim���� ���� ���� ������
git commit -a�ϸ� add�Ȱ�
git commit -am "[������� ��]"    �ϸ� �ٷ� ��
�� �ѹ��� �� add�� ���� ��쿡�� ���� ����

�귣ġ
�����Ϳ��� ���� �ϳ� �����Ŀ� ���� ����
git branch
git branch [�̸�]    = ����
git checkout [�̸�]  = �귣ġ ����� ����(�⺻ = master)
git checkout -b [�̸�] = ������ ����

�귣ġ ���� ����
git log --branches	--decorate --graph --oneline

���̺���
git log master..exp   : master���� ���� exp���� �ִ°� ���' 
git log -p exp..master : exp���� ���� master���ִ°��� ������ְ�
exp���� ���°��� --�� ��� master�� �ִ°� ++ �װ��� ���� +�� ����
  
git diff master..exp



����
exp�� ������� master�� �Űܺ���
git merge exp

exp ����� 
git branch -d exp
�������� ������ ���� = �浹
�ٸ� ���� ���� = ����..?
�浹���� ���� �����ؾ���

stash? comiit���� �ʰ� ���� �ϰ� ������
���ϵ� Ŀ�� ���� ������ ���� �귣ġ�� �ִ°͵� �ڵ����� �������� ��
Ŀ���ؾ� ���� ��� ����
git stash �ϸ� ��(���̱�...?)
git stash apply : �ǻ츮��~
git stash list : ���� ���
git stash drop :��� ���� �ֽ� �� ���̱� 0����
git stash pop : apply �Ǹ鼭 drop�� ��

���� ����� �����
git init local
���� ����� 
git init --bare remote
: �۾��� �ȵǰ� ���常 ������ remote ���͸� ����
git remote add origin /c/Users/bohee/desktop/programming/git/remote
���� /�� ������ �ȵ� ex ) remote/


origin�� �������� ����� ������ ��
���� Ȯ��
git remote -v
���� �����
git remote remove origin

git push
$ git config --global push.default simple
$ git push --set-upstream origin master
������  push �ϸ� origin�� �����ͷ�  push �ϰڴ�

�׷��� local�� ����� ���� ������ remote���� �ִ°� Ȯ��
------------���� ��ü�� �ִ°� �ƴ� git log ������ ����cd-----------------------------------


git�� �α��� �� fork �ϰ� clone or download���� �ּ� ����
git clone [�ּ�] [�� ���͸�]



�꿡 ���� ->��������
mkdir gfh�����
init �� ���� �߰� Ŀ�� ��

�ι�° ĭ���� ù �� ���� �� �ٿ� �ֱ�
git remote -v �غ���
git remote remove origin �ϸ� ���� ��

git push -u origin master
�� �α���
�ϸ� ������ push �ϸ� �ּҷ� �ö�

�ö� ���� ���� �ޱ�
clone and download���� �ּ� ����
�� ���͸� �����
git clone https://github.com/sungdoolim/gfh.git .
���⼭ . �� �� ���͸�


commit �޽��� ���� �ϱ� 
git commit --amend �ϸ� vi���� ��

��������
git clone [�ּ�] [�����̸�]
�� �ȿ��� git pull


ssh-keygen
�ϰ� ���Ϳ����;���
��� ���  (/c/Users/bohee/.ssh/id_rsa)
cd ~/.ssh�� ������
�ϸ� �ΰ� ���� private / public
local ���� private�� �����
���� ����ҿ��� public�� �����

git tag [��ũĿ��Ʈ] [�ּ�]
Ŀ��Ʈ �±װ� �޸�
git checkout [��ũĿ��Ʈ]


�±� ���� �߰�
git tag -a [1.1.0] -m "bug fix" [�ּ�]
git tag -v [tag�̸�] �ϸ� bugfix ����

1.1.0�̶�� �±׸� �ְ�
git tag -v 1.1.0---------------------------------------
�ϸ� bug fix ���

�±׵� �ø����� git push --tags
����
git tag -d 1.1.0


git rebase master
merge�� ��������� �����


















