# citypassenger_qrcode

## How to use qr_code in angular :

#### If you use npm :

- `npm i citypassenger_qrcode`
- In angular.json add 

  ```
  project_name :{ 
    architect: { 
      build: { 
        options: { 
          scripts: [
            "node_modules/citypassenger_qrcode/qr_code.js",
            ...
          ] 
        }
      }
    }
  }
  ```

#### If you download the file :

- Add `qr_code.js` to your_project/src/assets
- In angular.json add 

  ```
  project_name :{ 
    architect: { 
      build: { 
        options: { 
          scripts: [
            "projects/landing/src/assets/qr_code.js",
            ...
          ] 
        }
      }
    }
  }
  ```
#### Then

- 

- inside component.html, create a div with `#aNameForQrCodeContainer`

- inside component.ts:
  - `declare function wfqr(name, password, encryption, divElement): any;` above `@Component`
  - add `  @ViewChild('aNameForQrCodeContainer', { static: true }) qrCodeContainer: ElementRef;`
  
- now you can use

  ```
  ngOnInit(){  
    wfqr(name, encryption, password, this.qrCodeContainer.nativeElement)  
  }
  ```
