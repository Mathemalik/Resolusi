#include <iostream>

using namespace std;

int main()
{
	// proses input nama
	string nama;
	int usia;
	cout <<"masukan nama :";
	getline(cin,nama);
	cout <<"masukan usia :";
	cin >> usia;
	cout <<"Nama :"<< nama;
	cout <<"\nUsia :"<<usia;
	if (usia<=3){
		cout << "\n\nTIDAK BOLEH MENONTON!!!"<< endl;
	}else if(usia<17){
		cout << "\n\nSILAHKAN PILIH FILM!!" << endl;
	}
	
	{
	int pilihan,angka;
	kembali:
	do
{
cout<<"\n\n\n\t*==============================*";cout<<endl;
cout<<"\t||Dafar Pemesanan Tiket 21 ||";cout<<endl;
cout<<"\t*==============================*";cout<<endl; cout<<endl;
cout<<"\tDAFTAR MENU ";cout<<endl;
cout<<"\t1. anak-anak             "<<endl;
cout<<"\t2. komedi remaja             "<<endl;
cout<<"\t3. dewasa    "<<endl;
cout<<"\t4. Keluar                     "<<endl;
cout<<endl;
cout<<" Masukan Pilihan Anda (1-4) : ";cin>>pilihan;
cout<<endl;
   
     switch (pilihan)
{
    case 1:
     mulai:
     int jenisTKT,jumlahTKT,totalTKT;
     char* jenisTXT;
     char ulang,belanjaKmbl;
   
       cout<<" ===================================================="<<endl;
       cout<<"\t   Pembelian Tiket ";cout<<endl;
       cout<<" ===================================================="<<endl;
     
    cout<<" Keterangan"<<endl;
    cout<<" 1. jam tayang 10:00"<<endl;
    cout<<" 2. jam tayang 13:20"<<endl;
    cout<<" 3. jam tayang 18:20"<<endl;
	cout<<" ===================================================="<<endl;
    cout<<" pilih jam tayang"<<endl;
    cout<<" Jenis Tiket (1-2)  : "; cin>>jenisTKT;
    cout<<" Jumlah Tiket   : "; cin>>jumlahTKT;cout<<endl;
    cout<<" ===================================================="<<endl;
    
     if (jenisTKT==1)
     {
      totalTKT=jumlahTKT*40000;
      jenisTXT="Dewasa";
     }
     else if (jenisTKT==2)
     {
     	totalTKT=jumlahTKT*35000;
     	jenisTXT="Tiket Komedi Dewasa";
	 }
     else if (jenisTKT==3)
     {
      totalTKT=jumlahTKT*25000;
      jenisTXT="Anak-anak";
}
	else
{
      cout<<" Angka Yang Anda Input Salah";
      cout<<endl;
      goto mulai;
}
   
       cout<<" Jenis Tiket   : "<<jenisTXT<<endl;
       cout<<" Jumlah Tiket   : "<<jumlahTKT<<"\n";
       cout<<" ----------------------------------------------------"<<endl;
       cout<<" Total Bayar   : Rp. "<<totalTKT<<endl;
       cout<<endl;
    break;
   
     
    case 2:
    int KursiTerisi[2],kursiKSONG[2];
       	cout<<" ======================================================="<<endl;
       	cout<<"\t   Cek Sisa Kursi ";cout<<endl;
       	cout<<" ======================================================="<<endl;
       	cout<<" Keterangan"<<endl;
       	cout<<" Jumlah Kursi Di Bioskop XXI Syntax404 sebangak 30 Kursi"<<endl;
       	cout<<" ======================================================="<<endl;
       	cout<<" Input Jumlah Kursi Yang Ingin Dipesan"<<endl;
    	angka=0;
	do
   
{
   
    cout<<" Jumlah Pemesanan Kursi  : ";
    cin>>KursiTerisi[angka];
	angka++;
   
}
   
    while (angka<1);
    for (angka=0;angka<1;angka++)
	    kursiKSONG[angka]=50-KursiTerisi[angka];
   
      cout<<" ===================================================="<<endl;
    for (angka=0;angka<1;angka++)
   
{
     
       cout<<" Sisa Kursi   : "<<kursiKSONG[angka];cout<<endl;
       cout<<" ===================================================="<<endl;
       cout<<endl;
} 
        break;
   
   case 3:
    	int tiketAnak[2],tiketDewasa[2],total[2];
    cout<<" ===================================================="<<endl;
    cout<<"\t   Input Laporan Penjualan Tiket ";cout<<endl;
    cout<<" ===================================================="<<endl;
	    for (angka=0;angka<2;angka++)
    {
    cout<<" Input Data Penjualan "<<angka+1<<endl;
    cout<<" Anak-anak   : "; cin>>tiketAnak[angka];
    cout<<" Dewasa    : "; cin>>tiketDewasa[angka];
    cout<<endl;
}
    for (angka=0;angka<2;angka++)
     total[angka]=tiketAnak[angka]+tiketDewasa[angka];
     cout<<" ===================================================="<<endl;
     cout<<"\t   Input Laporan Penjualan Tiket ";cout<<endl;
     cout<<" ===================================================="<<endl;
     cout<<" |Tiket  |  Anak-anak  |  Dewasa  |  Total Penjualan|"<<endl;
     cout<<" ----------------------------------------------------"<<endl;
     for (angka=0;angka<2;angka++)
    {
     cout<<" |  "<<angka+1<<"  "<<tiketAnak[angka]<<"          "<<tiketDewasa[angka];
     cout<<"  "<<total[angka]<<"           |"<<endl;
   
     }
     break;
   }
}
while (pilihan!=4);

}
	
	return 0;
}
