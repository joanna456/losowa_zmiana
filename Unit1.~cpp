//---------------------------------------------------------------------------

#include <vcl.h>
#pragma hdrstop

#include "Unit1.h"
//---------------------------------------------------------------------------
#pragma package(smart_init)
#pragma resource "*.dfm"
TForm1 *Form1;
bool gra_rozpoczeta = false;
int ile=0;
int liczby [1000]; // ilosc powtorzen

void sekwencja()
{
                Form1->z1a->Visible = false;
                Form1->z2a->Visible = false;
                Form1->z3a->Visible = false;
                Form1->z4a->Visible = false;
        ile++;
        for(int i=0;i<ile; i++)
        {
         switch(liczby[i])
                {
                case 1:
                Form1->z1a->Visible = true; break;
                case 2:
                Form1->z2a->Visible = true; break;
                case 3:
                Form1->z3a->Visible = true; break;
                case 4:
                Form1->z4a->Visible = true; break;
               }
               Application->ProcessMessages(); Sleep(1200);

               Form1->z1a->Visible = false;
               Form1->z2a->Visible = false;
               Form1->z3a->Visible = false;
               Form1->z4a->Visible = false;

               Application->ProcessMessages(); Sleep(1200);
               }


}
//---------------------------------------------------------------------------
__fastcall TForm1::TForm1(TComponent* Owner)
        : TForm(Owner)
{
}
//---------------------------------------------------------------------------


void __fastcall TForm1::FormCreate(TObject *Sender)
{
        randomize();
        for(int i=0; i<1000; i++)
        {
                liczby[i] = random(4)+1;
        }
}

//---------------------------------------------------------------------------
void __fastcall TForm1::tloClick(TObject *Sender)
{
  if(gra_rozpoczeta == false)
                gra_rozpoczeta = true;
                sekwencja();

}
//---------------------------------------------------------------------------


void __fastcall TForm1::z1aMouseDown(TObject *Sender, TMouseButton Button,
      TShiftState Shift, int X, int Y)
{
if(z1a->Canvas->Pixels[X][Y] != clWhite)
        z1a->Picture->LoadFromFile("images/p1a.bmp");
}
//---------------------------------------------------------------------------




