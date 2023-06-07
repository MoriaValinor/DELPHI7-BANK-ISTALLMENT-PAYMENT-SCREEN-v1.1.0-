unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, StdCtrls, ComCtrls;

type
  TForm1 = class(TForm)
    DateTimePicker1: TDateTimePicker;
    Label2: TLabel;
    Label3: TLabel;
    Label4: TLabel;
    Edit1: TEdit;
    Edit3: TEdit;
    Edit4: TEdit;
    Button1: TButton;
    Label1: TLabel;
    ListBox1: TListBox;
    Label5: TLabel;
    Label6: TLabel;
    Edit2: TEdit;
    procedure Edit3Change(Sender: TObject);
    procedure Button1Click(Sender: TObject);
  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;
  i:integer;
implementation

{$R *.dfm}

procedure TForm1.Edit3Change(Sender: TObject);
begin
if(Trim(Edit3.Text)<>'')then begin
if(StrToInt(Trim(Edit3.Text))<2)or (StrToInt(Trim(Edit3.Text))>8)then begin
Application.MessageBox('Installments must be between 2 and 8 months','INSTALLMENT ERROR');
end;
end;
end;

procedure TForm1.Button1Click(Sender: TObject);
begin
if(Trim(Edit1.Text)<>'') and (Trim(Edit3.Text)<>'')and
(Trim(Edit4.Text)<>'') then begin
ListBox1.Clear;

for i:=1 to StrToInt(Edit3.Text)do begin
ListBox1.Items.Add((DateToStr(IncMonth((DateTimePicker1.Date),i) ))+'                 '+
FloatToStr((StrToInt(Edit1.Text)-StrToInt(Edit4.Text)) / StrToInt(Edit3.Text))+' $');
end;
ListBox1.Items.Add('-----------------------------------------------------');
ListBox1.Items.Add('Total Debt Amount  : '+Edit1.Text+' $');
end else begin
ShowMessage('Complete [ Total Debt - Advance Payment - Number of Installments ]');
Edit1.SetFocus;
end;
end;
end.
