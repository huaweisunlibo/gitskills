http://blog.csdn.net/x728999452/article/details/50759249

https://gpg4win.org/download.html

windows��GPG��ʹ��
ԭ�� 2016��02��28�� 11:16:14 2925
GPG��GNU PrivacyGuard�����Ǽ��ܹ���PGP��Pretty Good Privacy���ķ���ҵ���汾�����ڶ�Email���ļ����������ݵ��շ����м�������֤��ȷ��ͨ�����ݵĿɿ��Ժ���ʵ�ԡ�
һ��GPG�İ�װ
��������:www.gnupg.org

����GPG��ʹ��
1.������Կ�ԣ��������������������
gpg --gen-key
ϵͳ��ѯ�����ơ��������䣬������ɺ󽫵����Ի���

����Passphrase�������ṩ����������Ҫ�����˽Կ���������޷�ʹ�ã���

2.�г���Կ���������������������
gpg --list-keys

3.������Կ���������������������
gpg --export -armor -o filename(�ļ�Ŀ¼��  F:\file.txt)
����
gpg --export -a > filename
����Կ�������ļ����Ա���������ʹ�á�
-armorѡ�ͬ-aѡ����ı���ʽ��ʾ��������Ƕ����Ƹ�ʽ��

4.���빫Կ���������������������
gpg --import filename
 
���������˵Ĺ�Կ

5.�����ļ����������������������
gpg --encrypt -armor -r key-id filename
��key-id�Ĺ�Կ������Ϣ�����δ�ṩ-r key-id�������ʾ�ռ������롣Ĭ������ļ�Ϊfilename.asc��

6.�����ļ����������������������
gpg --output ���ļ��� --decrypt �����ļ���
������ʾ����Passphrase��

7.�޸���Կ���������������������
gpg --edit-key ��ʶ��

8.ɾ����Կ���������������������
������ɾ��˽Կ��Ȼ�����ɾ����Կ��
�������������������
gpg --delete-secret-keys ��ʶ��
gpg --delete-keys ��ʶ��