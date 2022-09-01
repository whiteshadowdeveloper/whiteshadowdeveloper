#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;


float birim_fiyat = (206.0 / 100.0);
float ort_enerji_app = 30.0;
float ort_enerji_ap = 44.0;
float ort_enerji_a = 58.0;
float ort_enerji_b = 73.0;
float ort_enerji_c = 96.0;
float ort_enerji_d = 106.0;
float ort_enerji_e = 132.0;


void hesapla_ve_yazdir (string enerji_sinifi, float gunluk_tuketim)
{

  float sonuc;
  float enerji_oran;

  cout << "hesapla ve yazdir " + enerji_sinifi;	

  if (enerji_sinifi == "A++")
    {
      cout << ("Mumkun olan en iyi enerji sinifini kullaniyorsunuz");
      cout << ("\n");
    }
  else if (enerji_sinifi == "A+")
    {

      enerji_oran = ort_enerji_ap / ort_enerji_app;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A++ sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

    }
  else if (enerji_sinifi == "A")
    {

      enerji_oran = float (ort_enerji_a / ort_enerji_app);
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A++ sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_a / ort_enerji_ap;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A+ sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

    }
  else if (enerji_sinifi == "B")
    {

      enerji_oran = ort_enerji_b / ort_enerji_app;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A++ sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_b / ort_enerji_ap;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A+ sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_b / ort_enerji_a;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

    }
  else if (enerji_sinifi == "C")
    {

      enerji_oran = ort_enerji_c / ort_enerji_app;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A++ sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_c / ort_enerji_ap;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A+ sinifa gecerseniz " + to_string (sonuc) + " tl  kadar kar edersiniz");

      enerji_oran = ort_enerji_c / ort_enerji_a;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_c / ort_enerji_b;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("B sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

    }
  else if (enerji_sinifi == "D")
    {

      enerji_oran = ort_enerji_d / ort_enerji_app;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A++ sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_d / ort_enerji_ap;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A+ sinifa gecerseniz " + to_string (sonuc) + "tl  kadar kar edersiniz");

      enerji_oran = ort_enerji_d / ort_enerji_a;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A sinifa gecerseniz " + to_string (sonuc) + "tl  kadar kar edersiniz");

      enerji_oran = ort_enerji_d / ort_enerji_b;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("B sinifa gecerseniz " + to_string (sonuc) + " tl  kadar kar edersiniz");

      enerji_oran = ort_enerji_d / ort_enerji_c;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("C sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

    }
  else if (enerji_sinifi == "E")
    {

      enerji_oran = ort_enerji_e / ort_enerji_app;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A++ sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_e / ort_enerji_ap;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A+ sinifa gecerseniz " + to_string (sonuc) + " tl  kadar kar edersiniz");

      enerji_oran = ort_enerji_e / ort_enerji_a;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("A sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_e / ort_enerji_b;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("B sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_e / ort_enerji_c;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("C sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

      enerji_oran = ort_enerji_e / ort_enerji_d;
      sonuc = (gunluk_tuketim - (gunluk_tuketim / enerji_oran)) * birim_fiyat;
      cout << ("\n");
      cout << ("D sinifa gecerseniz " + to_string (sonuc) + " tl kadar kar edersiniz");

    }
  else
    {
      cout << ("\n");
      cout << ("Gecerli enerji sinifi girmelisiniz!");
    }

}


int main ()
{

  int cesit;

  cout << ("Merhaba. Makine cesit sayisini giriniz: ");
  cin >> cesit;

  float toplam = 0.0;
  float sayi[cesit];
  float fark[cesit];
  float para[cesit];
  float saat[cesit];
  string sinif[cesit];
  float elektric[cesit];
  float enerji_tuketim_cesit;

  for (int i = 0; i < cesit; i++)
    {

      cout << ("\n");
      cout << (" * Cesit-" + to_string (i + 1) + " *");
      cout << ("\n");
      cout << ("Makinenin saatlik tukettigi enerji  miktarini giriniz: ");
      cin >> elektric[i];
      cout << ("Kac tane makine var: ");
      cin >> sayi[i];
      cout << ("Makine gunde kac saat calisiyor: ");
      cin >> saat[i];
      cout << ("Makinenin enerji sinifini giriniz (A++, A+, A, B, C, D, E): ");
      cin >> sinif[i];

      para[i] = elektric[i] * sayi[i] * saat[i]/1000;
      enerji_tuketim_cesit = para[i] * birim_fiyat;
      cout << ("\n");
      cout << ("Gunluk enerji tuketiminiz : " + to_string (enerji_tuketim_cesit));
      cout << ("\n");


      hesapla_ve_yazdir (sinif[i], para[i]);


      toplam = toplam + enerji_tuketim_cesit;

    }

  cout << ("\n");
  cout << ("Sectiginiz makine cesitlerinin toplam gunluk enerji tuketimi : " + to_string (toplam));
  cout << ("\n\n");
  cout << (" * iyi gunler *");
}
