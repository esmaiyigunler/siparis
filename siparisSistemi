class Siparis:
    def __init__(self,urunAdi,miktar,fiyat):
        self.urunAdi=urunAdi
        self.miktar=miktar
        self.fiyat=fiyat
    def toplamHesapla(self):
        return self.miktar* self.fiyat
class Musteri:
    def __init__(self,isim):
        self.isim=isim
        self.siparisler=[]
    def siparisEkle(self,siparis):
        self.siparisler.append(siparis)
    def siparisIptal(self,urunAdi):
        self.siparisler=[siparis for siparis in self.siparisler if siparis.urunAdi!=urunAdi]
    def toplamFaturaHesapla(self):
        return sum(siparis.toplamHesapla() for siparis in self.siparisler)
    def siparisleriGoster(self):
        print(f"{self.isim}'in siparişleri")
        for siparis in self.siparisler:
            print(f"{siparis.urunAdi}- {siparis.miktar} adet- {siparis.fiyat}TL")

musteri1=Musteri("Ali")
siparis1=Siparis("Pizza",2,50)
siparis2=Siparis("Hamburger",1,30)
musteri1.siparisEkle(siparis1)
musteri1.siparisEkle(siparis2)
musteri1.siparisleriGoster()
print(f"Toplam fatura:{musteri1.toplamFaturaHesapla()}TL")
musteri1.siparisIptal("Pizza")
musteri1.siparisleriGoster()
print(f"Güncel fatura:{musteri1.toplamFaturaHesapla()}TL")
