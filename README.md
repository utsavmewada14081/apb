# APB (Advanced Peripheral Bus)
The Advanced Peripheral Bus (APB) protocol is a low-power, non-pipelined, synchronous interface protocol in the ARM AMBA family designed for connecting low-bandwidth, peripheral devices (like UARTs, timers, GPIOs) to a system-on-chip (SoC). It uses a simple two-phase (Setup/Access) state machine, optimizing for low complexity rather than high speed.

## APB Signals

<table>
  <th>Signal</th>
  <th>Description</th>
  <tr>
    <td>PCLK</td>
    <td>The rising edge of PCLK times all transfers on the APB. System clock may be directly connected to PCLK</td>
  </tr>
  <tr>
    <td>PRESETn</td>
    <td>Active low asynchronous reset</td>
  </tr>
  <tr>
    <td>PADDR[31:0]</td>
    <td>Address bus from master to slave (32-bit wide)</td>
  </tr>
  <tr>
    <td>PWDATA[31:0]</td>
    <td>Write data bus from master to slave</td>
  </tr>
  <tr>
    <td>PRDATA[31:0]</td>
    <td>Read data bus from slave to master</td>
  </tr>
  <tr>
    <td>PSELx</td>
    <td>Slave select, one PSEL signal for each slave connected to master</td>
  </tr>
  <tr>
    <td>PENABLE</td>
    <td>Indicates the second and subsequent cycles of transfer</td>
  </tr>
  <tr>
    <td>PWRITE</td>
    <td>High (1) indicates write, Low (0) indicates read</td>
  </tr>
  <tr>
    <td>PREADY</td>
    <td>Slave signal high when slave is ready. Low means slave is not ready (wait states)</td>
  </tr>
  <tr>
    <td>PSLVERR</td>
    <td>Slave signal high indicates failure and low indicates successful transfer</td>
  </tr>
</table>


