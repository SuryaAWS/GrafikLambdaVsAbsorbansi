unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, StdCtrls, Series, TeEngine, ExtCtrls, TeeProcs, Chart, TeeFunci;

type
  TForm1 = class(TForm)
    Chart1: TChart;
    Series1: TLineSeries;
    Chart2: TChart;
    Label1: TLabel;
    Label2: TLabel;
    Edit1: TEdit;
    Edit2: TEdit;
    Memo1: TMemo;
    Button1: TButton;
    Button2: TButton;
    Bevel1: TBevel;
    Label3: TLabel;
    Label4: TLabel;
    Edit3: TEdit;
    Edit4: TEdit;
    Bevel2: TBevel;
    Memo2: TMemo;
    Chart3: TChart;
    Button3: TButton;
    Series3: TLineSeries;
    Series4: TLineSeries;
    Series2: TLineSeries;
    Label5: TLabel;
    procedure Memo1Change(Sender: TObject);
    procedure Button2Click(Sender: TObject);
    procedure Button1Click(Sender: TObject);
    procedure Button3Click(Sender: TObject);
    procedure Memo2Change(Sender: TObject);
  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;
  Data: array of real;

implementation

{$R *.dfm}

procedure TForm1.Memo1Change(Sender: TObject);
begin
    if edit1.Text='11' then
    memo1.ScrollBars:=ssVertical;
end;

procedure TForm1.Button2Click(Sender: TObject);
begin
    application.Terminate;
end;

procedure TForm1.Button1Click(Sender: TObject);
begin
    if edit2.Text='' then
      messagedlg('Data belum diisi boss',mtError,[mbok],0)
    else
    begin


      setlength(data,strtoint(edit1.Text)+10);
      data[strtoint(edit1.Text)]:=strtofloat(edit2.Text);
      series1.AddXY(strtoint(edit1.Text),strtofloat(edit2.Text),'',clred);
      memo1.Lines.Add(edit1.Text+'--->'+edit2.Text);
      edit1.Text:=inttostr(strtoint(edit1.Text)+10);
      edit2.Text:=floattostr(strtofloat(edit2.Text));
      edit2.Text:='';
      edit2.SetFocus;
      end;
end;

procedure TForm1.Button3Click(Sender: TObject);
begin
    if edit4.Text='' then
      messagedlg('Data belum diisi boss',mtError,[mbok],0)
    else
    begin
      setlength(data,strtoint(edit3.Text)+10);
      data[strtoint(edit3.Text)]:=strtofloat(edit4.Text);
      series2.AddXY(strtoint(edit3.Text),strtofloat(edit4.Text),'',clblue);
      memo2.Lines.Add(edit3.Text+'--->'+edit4.Text);
      edit3.Text:=inttostr(strtoint(edit3.Text)+10);
      edit4.Text:=floattostr(strtofloat(edit4.Text));
      edit4.Text:='';
      edit4.SetFocus;
      end;

end;

procedure TForm1.Memo2Change(Sender: TObject);
begin
    if edit3.Text='11' then
    memo2.ScrollBars:=ssVertical;

end;

end.
