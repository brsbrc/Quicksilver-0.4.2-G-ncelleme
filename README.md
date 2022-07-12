# Quicksilver-0.4.2-G-ncelleme

Güncelleme bloğuna geldiyseniz sırasıyla yapabilirsiniz arkadaşlar. Şunu unutmayalım, ilgili blok gelmeden önce yani aceleyle güncellemeyi yapmak kesinlikle size bir artı sağlamaz aksine hata alırsınız. Acele etmemenizi tavsiye ediyorum.

Blok, 212.000 olmadan yapmayın kesinlikle.

Güncelleme yapmak için log kaydında "ERR UPGRADE "upgrade-v0.4.2" NEEDED at height: 212000" uyarısını görmelisiniz.

Log kaydına bakmak için;
'''
journalctl -u quicksilverd -f -o cat
'''

1) sudo systemctl stop quicksilverd
2) sudo su
3) cd
4) rm -rf quicksilver 
5) git clone https://github.com/ingenuity-build/quicksilver.git
6) cd quicksilver
7) git checkout v0.4.2
8) make build
9) sudo chmod +x ./build/quicksilverd && sudo mv ./build/quicksilverd /usr/local/bin/quicksilverd
10) sudo systemctl restart quicksilverd

Güncellemeyi yaptıktan sonra teyit etmek için;

quicksilverd version

yazdıktan sonra gelen çıktı 0.4.2'yse tamamdır.
