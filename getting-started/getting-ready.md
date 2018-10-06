# Hardware Requirements

Due to the nature of packet analysis and granular drill-down, we're providing; Sensei require more horsepower than a standard opensource firewall installation.

{% hint style="info" %}
Sensei requires at least 8 GB of memory, please do not try to run the product on a system below 8GB of memory. 
{% endhint %}

## CPU & Memory

Because the analytics module relies on Elastic Search to do Big Data processing, amount of the memory available in the system is crucial for the performance of the whole product.

At least dual-core \(i5 and equivalent\) or preferably quad-core modern CPU \(i7 and equivalent\) would be advisable.

Recommended minimum hardware requirements for Sensei based on the number of users and the bandwidth:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Number of Users</th>
      <th style="text-align:left">WAN Bandwith</th>
      <th style="text-align:left">Min. Memory</th>
      <th style="text-align:left">Min. CPU</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <25</td>
          <td style="text-align:left">20 Mbps</td>
          <td style="text-align:left">8 GB</td>
          <td style="text-align:left">Intel Dual-Core i3 2.0 GHz (2 Cores, 4 Threads) or equivalent</td>
    </tr>
    <tr>
      <td style="text-align:left">25-50</td>
      <td style="text-align:left">50 Mbps
        <br />10 Kpps</td>
      <td style="text-align:left">8 GB</td>
      <td style="text-align:left">Intel Dual-Core i5 2.0 GHz (2 Cores, 4 Threads) or equivalent</td>
    </tr>
    <tr>
      <td style="text-align:left">50-100</td>
      <td style="text-align:left">
        <p>100 Mbps</p>
        <p>20 Kpps</p>
      </td>
      <td style="text-align:left">16 GB</td>
      <td style="text-align:left">Intel Dual-Core i5 2.2 GHz (2 Cores, 4 Threads) or equivalent</td>
    </tr>
    <tr>
      <td style="text-align:left">100-250</td>
      <td style="text-align:left">
        <p>200 Mbps</p>
        <p>40 Kpps</p>
      </td>
      <td style="text-align:left">16 GB</td>
      <td style="text-align:left">Intel Dual-Core i7 2.0 GHz (2 Cores, 4 Threads) or equivalent</td>
    </tr>
    <tr>
      <td style="text-align:left">250-1000</td>
      <td style="text-align:left">
        <p>500 Mbps</p>
        <p>100 Kpps</p>
      </td>
      <td style="text-align:left">32 GB</td>
      <td style="text-align:left">Intel <b>Quad</b>-Core i7 3.40 GHz (4 Cores, 8 Threads) or equivalent</td>
    </tr>
  </tbody>
</table>## Disk Space

{% hint style="info" %}
Sensei uses [Elastic Search Engine](https://en.wikipedia.org/wiki/Elasticsearch%20) as its backend to process the Big Data. Please spare at least 5 MB of disk space per hour per megabit/second throughput.
{% endhint %}

If you're running a 100 Mbps link \(about 100 users\) which is quite active during the daytime and idle rest of the day, you can calculate the space needed as follows:

```
5 MB x 12 hours x 100 Mbps = 6 GB per day.
6 GB x 7 days a week = 42 GB per week.
42 x 4 weeks a month = 164 GB per month.
```

As of 0.7.0 \([_changelog_](https://www.sunnyvalley.io/blog/what-s-cooking-for-0-7)\), Sensei retires reports data to open up space for the new ones. After a configured timespan, existing reports data automatically purges to save space for fresh data.

