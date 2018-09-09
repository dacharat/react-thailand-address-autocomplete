# react-thailand-address-autocomplete
Auto-complete Thailand address input component for React.js


<img src="https://raw.githubusercontent.com/winChawakorn/react-thailand-address-autocomplete/master/assets/react-thailand-address-autocomplete.gif" height="350px" />

## Insallation
**yarn**
```
yarn add react-thailand-address-autocomplete
```
**npm**
```
npm install --save react-thailand-address-autocomplete
```
## Usage
```js
import InputAddress from 'react-thailand-address-autocomplete'
```
```js
  onChange(e) {
    this.setState({
      [e.target.name]: e.target.value
    })
  }

  onSelect(fullAddress) {
    const { subdistrict, district, province, zipcode } = fullAddress
    this.setState({
      subdistrict,
      district,
      province,
      zipcode
    })
  }

  render() {
    return (
      <div>
        แขวง / ตำบล
        <InputAddress
          address="subdistrict"
          value={this.state.subdistrict}
          onChange={this.onChange}
          onSelect={this.onSelect}
        />
        เขต / อำเภอ
        <InputAddress
          address="district"
          value={this.state.district}
          onChange={this.onChange}
          onSelect={this.onSelect}
        />
      </div>
    );
  }
```
