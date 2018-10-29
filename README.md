<!-- DO NOT EDIT THIS FILE MANUALLY. This file is generated by generate_readme.py from conversions.yaml so please edit and run them. -->
# PyTorch for Numpy users.

[![Build Status](https://travis-ci.org/wkentaro/pytorch-for-numpy-users.svg?branch=master)](https://travis-ci.org/wkentaro/pytorch-for-numpy-users)

[PyTorch](https://github.com/pytorch/pytorch.git) version of [_Torch for Numpy users_](https://github.com/torch/torch7/wiki/Torch-for-Numpy-users).  
We assume you use the latest PyTorch and Numpy.


## How to contribute?

```bash
git clone https://github.com/wkentaro/pytorch-for-numpy-users.git
cd pytorch-for-numpy-users
vim conversions.yaml
git commit -m "Update conversions.yaml"

./run_tests.py
```


## Types

<table>
<thead>
<tr><th>Numpy                  </th><th>PyTorch                                 </th></tr>
</thead>
<tbody>
<tr><td><code>np.ndarray</code></td><td><code>torch.Tensor</code>               </td></tr>
<tr><td><code>np.float32</code></td><td><code>torch.float32; torch.float</code> </td></tr>
<tr><td><code>np.float64</code></td><td><code>torch.float64; torch.double</code></td></tr>
<tr><td><code>np.float16</code></td><td><code>torch.float16; torch.half</code>  </td></tr>
<tr><td><code>np.int8</code>   </td><td><code>torch.int8</code>                 </td></tr>
<tr><td><code>np.uint8</code>  </td><td><code>torch.uint8</code>                </td></tr>
<tr><td><code>np.int16</code>  </td><td><code>torch.int16; torch.short</code>   </td></tr>
<tr><td><code>np.int32</code>  </td><td><code>torch.int32; torch.int</code>     </td></tr>
<tr><td><code>np.int64</code>  </td><td><code>torch.int64; torch.long</code>    </td></tr>
</tbody>
</table>


## Constructors

### Ones and zeros

<table>
<thead>
<tr><th>Numpy                        </th><th>PyTorch                         </th></tr>
</thead>
<tbody>
<tr><td><code>np.empty((2, 3))</code></td><td><code>torch.empty(2, 3)</code>  </td></tr>
<tr><td><code>np.empty_like(x)</code></td><td><code>torch.empty_like(x)</code></td></tr>
<tr><td><code>np.eye</code>          </td><td><code>torch.eye</code>          </td></tr>
<tr><td><code>np.identity</code>     </td><td><code>torch.eye</code>          </td></tr>
<tr><td><code>np.ones</code>         </td><td><code>torch.ones</code>         </td></tr>
<tr><td><code>np.ones_like</code>    </td><td><code>torch.ones_like</code>    </td></tr>
<tr><td><code>np.zeros</code>        </td><td><code>torch.zeros</code>        </td></tr>
<tr><td><code>np.zeros_like</code>   </td><td><code>torch.zeros_like</code>   </td></tr>
</tbody>
</table>

### From existing data

<table>
<thead>
<tr><th>Numpy                                                                     </th><th>PyTorch                                                   </th></tr>
</thead>
<tbody>
<tr><td><code>np.array([[1, 2], [3, 4]])</code>                                   </td><td><code>torch.tensor([[1, 2], [3, 4]])</code>               </td></tr>
<tr><td><pre>
np.array([3.2, 4.3], dtype=np.float16)
np.float16([3.2, 4.3])
</pre></td><td><code>torch.tensor([3.2, 4.3], dtype=torch.float16)</code></td></tr>
<tr><td><code>x.copy()</code>                                                     </td><td><code>x.clone()</code>                                    </td></tr>
<tr><td><code>np.fromfile(file)</code>                                            </td><td><code>torch.tensor(torch.Storage(file))</code>            </td></tr>
<tr><td><code>np.frombuffer</code>                                                </td><td>                                                          </td></tr>
<tr><td><code>np.fromfunction</code>                                              </td><td>                                                          </td></tr>
<tr><td><code>np.fromiter</code>                                                  </td><td>                                                          </td></tr>
<tr><td><code>np.fromstring</code>                                                </td><td>                                                          </td></tr>
<tr><td><code>np.load</code>                                                      </td><td><code>torch.load</code>                                   </td></tr>
<tr><td><code>np.loadtxt</code>                                                   </td><td>                                                          </td></tr>
<tr><td><code>np.concatenate</code>                                               </td><td><code>torch.cat</code>                                    </td></tr>
</tbody>
</table>

### Numerical ranges

<table>
<thead>
<tr><th>Numpy                            </th><th>PyTorch                             </th></tr>
</thead>
<tbody>
<tr><td><code>np.arange(10)</code>       </td><td><code>torch.arange(10)</code>       </td></tr>
<tr><td><code>np.arange(2, 3, 0.1)</code></td><td><code>torch.arange(2, 3, 0.1)</code></td></tr>
<tr><td><code>np.linspace</code>         </td><td><code>torch.linspace</code>         </td></tr>
<tr><td><code>np.logspace</code>         </td><td><code>torch.logspace</code>         </td></tr>
</tbody>
</table>

### Building matrices

<table>
<thead>
<tr><th>Numpy               </th><th>PyTorch                </th></tr>
</thead>
<tbody>
<tr><td><code>np.diag</code></td><td><code>torch.diag</code></td></tr>
<tr><td><code>np.tril</code></td><td><code>torch.tril</code></td></tr>
<tr><td><code>np.triu</code></td><td><code>torch.triu</code></td></tr>
</tbody>
</table>

### Attributes

<table>
<thead>
<tr><th>Numpy                 </th><th>PyTorch                  </th></tr>
</thead>
<tbody>
<tr><td><code>x.shape</code>  </td><td><code>x.shape</code>     </td></tr>
<tr><td><code>x.strides</code></td><td><code>x.stride()</code>  </td></tr>
<tr><td><code>x.ndim</code>   </td><td><code>x.dim()</code>     </td></tr>
<tr><td><code>x.data</code>   </td><td><code>x.data</code>      </td></tr>
<tr><td><code>x.size</code>   </td><td><code>x.nelement()</code></td></tr>
<tr><td><code>x.dtype</code>  </td><td><code>x.dtype</code>     </td></tr>
</tbody>
</table>

### Indexing

<table>
<thead>
<tr><th>Numpy                           </th><th>PyTorch                                              </th></tr>
</thead>
<tbody>
<tr><td><code>x[0]</code>               </td><td><code>x[0]</code>                                    </td></tr>
<tr><td><code>x[:, 0]</code>            </td><td><code>x[:, 0]</code>                                 </td></tr>
<tr><td><code>x[indices]</code>         </td><td><code>x[indices]</code>                              </td></tr>
<tr><td><code>np.take(x, indices)</code></td><td><code>torch.take(x, torch.LongTensor(indices))</code></td></tr>
<tr><td><code>x[x != 0]</code>          </td><td><code>x[x != 0]</code>                               </td></tr>
</tbody>
</table>

### Shape manipulation

<table>
<thead>
<tr><th>Numpy                                              </th><th>PyTorch                              </th></tr>
</thead>
<tbody>
<tr><td><code>x.reshape</code>                             </td><td><code>x.reshape; x.view</code>       </td></tr>
<tr><td><code>x.resize()</code>                            </td><td><code>x.resize_</code>               </td></tr>
<tr><td>                                                   </td><td><code>x.resize_as_</code>            </td></tr>
<tr><td><code>x.transpose</code>                           </td><td><code>x.transpose or x.permute</code></td></tr>
<tr><td><code>x.flatten</code>                             </td><td><code>x.view(-1)</code>              </td></tr>
<tr><td><code>x.squeeze()</code>                           </td><td><code>x.squeeze()</code>             </td></tr>
<tr><td><code>x[:, np.newaxis]; np.expand_dims(x, 1)</code></td><td><code>x.unsqueeze(1)</code>          </td></tr>
</tbody>
</table>

### Item selection and manipulation

<table>
<thead>
<tr><th>Numpy                                                                 </th><th>PyTorch                                                                                                                                               </th></tr>
</thead>
<tbody>
<tr><td><code>np.put</code>                                                   </td><td>                                                                                                                                                      </td></tr>
<tr><td><code>x.put</code>                                                    </td><td><code>x.put_</code>                                                                                                                                   </td></tr>
<tr><td><pre>
x = np.array([1, 2, 3])
x.repeat(2)  # [1, 1, 2, 2, 3, 3]
</pre></td><td><pre>
x = torch.tensor([1, 2, 3])
x.repeat(2)  # [1, 2, 3, 1, 2, 3]
x.repeat(2).reshape(2, -1).transpose(1, 0).reshape(-1)
# [1, 1, 2, 2, 3, 3]
</pre></td></tr>
<tr><td><code>np.tile(x, (3, 2))</code>                                       </td><td><code>x.repeat(3, 2)</code>                                                                                                                           </td></tr>
<tr><td><code>np.choose</code>                                                </td><td>                                                                                                                                                      </td></tr>
<tr><td><code>np.sort</code>                                                  </td><td><code>sorted, indices = torch.sort(x, [dim])</code>                                                                                                   </td></tr>
<tr><td><code>np.argsort</code>                                               </td><td><code>sorted, indices = torch.sort(x, [dim])</code>                                                                                                   </td></tr>
<tr><td><code>np.nonzero</code>                                               </td><td><code>torch.nonzero</code>                                                                                                                            </td></tr>
<tr><td><code>np.where</code>                                                 </td><td><code>torch.where</code>                                                                                                                              </td></tr>
<tr><td><code>x[::-1]</code>                                                  </td><td><code>torch.flip(x, [0])</code>                                                                                                                       </td></tr>
</tbody>
</table>

### Calculation

<table>
<thead>
<tr><th>Numpy                   </th><th>PyTorch                                    </th></tr>
</thead>
<tbody>
<tr><td><code>x.min</code>      </td><td><code>x.min</code>                         </td></tr>
<tr><td><code>x.argmin</code>   </td><td><code>x.argmin</code>                      </td></tr>
<tr><td><code>x.max</code>      </td><td><code>x.max</code>                         </td></tr>
<tr><td><code>x.argmax</code>   </td><td><code>x.argmax</code>                      </td></tr>
<tr><td><code>x.clip</code>     </td><td><code>x.clamp</code>                       </td></tr>
<tr><td><code>x.round</code>    </td><td><code>x.round</code>                       </td></tr>
<tr><td><code>np.floor(x)</code></td><td><code>torch.floor(x); x.floor()</code>     </td></tr>
<tr><td><code>np.ceil(x)</code> </td><td><code>torch.ceil(x); x.ceil()</code>       </td></tr>
<tr><td><code>x.trace</code>    </td><td><code>x.trace</code>                       </td></tr>
<tr><td><code>x.sum</code>      </td><td><code>x.sum</code>                         </td></tr>
<tr><td><code>x.cumsum</code>   </td><td><code>x.cumsum</code>                      </td></tr>
<tr><td><code>x.mean</code>     </td><td><code>x.mean</code>                        </td></tr>
<tr><td><code>x.std</code>      </td><td><code>x.std</code>                         </td></tr>
<tr><td><code>x.prod</code>     </td><td><code>x.prod</code>                        </td></tr>
<tr><td><code>x.cumprod</code>  </td><td><code>x.cumprod</code>                     </td></tr>
<tr><td><code>x.all</code>      </td><td><code>(x == 1).sum() == x.nelement()</code></td></tr>
<tr><td><code>x.any</code>      </td><td><code>(x == 1).sum() > 0</code>            </td></tr>
</tbody>
</table>

### Arithmetic and comparison operations

<table>
<thead>
<tr><th>Numpy                        </th><th>PyTorch          </th></tr>
</thead>
<tbody>
<tr><td><code>np.less</code>         </td><td><code>x.lt</code></td></tr>
<tr><td><code>np.less_equal</code>   </td><td><code>x.le</code></td></tr>
<tr><td><code>np.greater</code>      </td><td><code>x.gt</code></td></tr>
<tr><td><code>np.greater_equal</code></td><td><code>x.ge</code></td></tr>
<tr><td><code>np.equal</code>        </td><td><code>x.eq</code></td></tr>
<tr><td><code>np.not_equal</code>    </td><td><code>x.ne</code></td></tr>
</tbody>
</table>



