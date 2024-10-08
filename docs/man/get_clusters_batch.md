

# get_clusters_batch

[**Source code**](https://github.com/CSAFE-ISU/handwriter/tree/176-automatic-documentation/R/#L)

## Description

get_clusters_batch

## Usage

<pre><code class='language-R'>get_clusters_batch(
  template,
  input_dir,
  output_dir,
  writer_indices,
  doc_indices,
  num_cores = 1
)
</code></pre>

## Arguments

<table>
<tr>
<td style="white-space: nowrap; font-family: monospace; vertical-align: top">
<code id="template">template</code>
</td>
<td>
A cluster template created with <code>make_clustering_template</code>
</td>
</tr>
<tr>
<td style="white-space: nowrap; font-family: monospace; vertical-align: top">
<code id="input_dir">input_dir</code>
</td>
<td>
A directory containing graphs created with
<code>process_batch_dir</code>
</td>
</tr>
<tr>
<td style="white-space: nowrap; font-family: monospace; vertical-align: top">
<code id="output_dir">output_dir</code>
</td>
<td>
Output directory for cluster assignments
</td>
</tr>
<tr>
<td style="white-space: nowrap; font-family: monospace; vertical-align: top">
<code id="writer_indices">writer_indices</code>
</td>
<td>
Vector of start and end indices for the writer id in the graph file
names
</td>
</tr>
<tr>
<td style="white-space: nowrap; font-family: monospace; vertical-align: top">
<code id="doc_indices">doc_indices</code>
</td>
<td>
Vector of start and end indices for the document id in the graph file
names
</td>
</tr>
<tr>
<td style="white-space: nowrap; font-family: monospace; vertical-align: top">
<code id="num_cores">num_cores</code>
</td>
<td>
Integer number of cores to use for parallel processing
</td>
</tr>
</table>

## Value

A list of cluster assignments

## Examples

``` r
library(handwriter)

template <- readRDS('path/to/template.rds')
get_clusters_batch(template=template, input_dir='path/to/dir', output_dir='path/to/dir',
writer_indices=c(2,5), doc_indices=c(7,18), num_cores=1)

get_clusters_batch(template=template, input_dir='path/to/dir', output_dir='path/to/dir',
writer_indices=c(1,4), doc_indices=c(5,10), num_cores=5)
```
