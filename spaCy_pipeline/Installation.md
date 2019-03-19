```
conda install -c conda-forge spacy
python -m spacy download en_core_web_lg

# neural co-refresolution
# link - https://github.com/huggingface/neuralcoref
git clone https://github.com/huggingface/neuralcoref
cd neuralcoref
pip install Cython
pip install -e .
pip install https://github.com/huggingface/neuralcoref-models/releases/download/en_coref_lg-3.0.0/en_coref_lg-3.0.0.tar.gz
```

 



```python
        try:
            proc = subprocess.Popen(cmd,
                                    stdout=subprocess.PIPE,
                                    stderr=subprocess.PIPE,
                                    shell=shell)
            output, errmsg = proc.communicate()
            return_code = proc.returncode

        except OSError as e:
            return_code = e.errno
            errmsg = "Exception: %s, errmsg: '%s', return code: %i, cmd: %s" % \
                ('OSError',
                 e.strerror,
                 return_code,
                 cmd)
            self.set_err(errmsg)
            self.logger.debug(self.errmsg, exc_info=sys.exc_info())
            return (output, errmsg, return_code)
```

