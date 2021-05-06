# citypassenger_qrcode

## How to use qr_code in angular :

- Add qr_code.js inside your_project/src/assets

- inside component.html, create a div with `#aNameForQrCodeContainer`

- inside component.ts:
  - `declare function wfqr(name, password, encryption, divElement): any;` above `@Component`
  - add `  @ViewChild('aNameForQrCodeContainer', { static: true }) qrCodeContainer: ElementRef;`
  
- now you can use 
`ngOnInit(){  
  wfqr(name, encryption, password, this.qrCodeContainer.nativeElement)  
}`
