# urc
urc (Universal Remote Control) is an application (written for OpenWrt) that allows you to run a arbitrary scripts over TCP

# Configuration

# Protocol specification
            
<table>
  <thead>
    <tr>
      <th>Field lenght (bits)</th>
      <th>0</th><th>1</th><th>2</th><th>3</th><th>4</th><th>5</th><th>6</th><th>7</th><th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Byte 1</td>
      <td colspan="8">Packet ID</td>
      <td rowspan="3">Header</td>
    </tr>
    <tr>
      <td>Byte 2</td>
      <td colspan="8">Packet length</td>
    </tr>
    <tr>
      <td>Byte 3</td>
      <td colspan="2">User name (flag)</td>
      <td colspan="2">Pasword (flag)</td>
      <td colspan="4">Reserved</td>
    </tr>
    <tr>
      <td>Byte n</td>
      <td colspan="8">Action</td>
      <td rowspan="4">Body</td>
    </tr>
    <tr>
      <td>Byte n</td>
      <td colspan="8">Params</td>
    </tr>
    <tr>
      <td>Byte n</td>
      <td colspan="8">User name</td>
    </tr>
    <tr>
      <td>Byte n</td>
      <td colspan="8">Pasword</td>
    </tr>
    <tr>
      <td>Byte n</td>
      <td colspan="8" rowspan="2">CRC16</td>
      <td rowspan="2">Footer</td>
    </tr>
    <tr>
      <td>Byte n + 1</td>
    </tr>
  </tbody>
</table>
