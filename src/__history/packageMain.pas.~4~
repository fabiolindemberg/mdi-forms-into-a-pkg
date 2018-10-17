unit packageMain;

interface

uses
  Forms, UMDIChild;

var
  OldApplication : TApplication;
  OldScrean : TScreen;
  Form : TMDIChildPkg;

implementation

procedure AbreForm( Ap : TApplication; Sc : TScreen ); stdcall;
begin

  if (OldApplication = nil) and (OldScrean = nil) then begin
    OldApplication := Application;
    OldScrean := Screen;

    Application := Ap;
    Screen := Sc;
  end;

  Form := TMDIChildPkg.Create(Application);
  Form.SetParentComponent(Application.MainForm);
  Form.Show;

end;

procedure RetornaTudo; stdcall;
begin
  Application := OldApplication;
  Screen := OldScrean;
end;


Exports
  AbreForm,
  RetornaTudo;

begin
end.

end.
