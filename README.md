# eeeea-> Scanning keyvault service Traceback (most recent call last):
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\alive_progress\core\progress.py", line 343, in __alive_bar
    yield bar_handle if not _sampling else locals()
  File "C:\Users\v562455\Downloads\i\prowler\lib\check\check.py", line 541, in execute_checks
    lib = import_check(check_module_path)
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\prowler\lib\check\check.py", line 324, in import_check
    lib = importlib.import_module(f"{check_path}")
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\AppData\Local\Programs\Python\Python312\Lib\importlib\__init__.py", line 90, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "<frozen importlib._bootstrap>", line 1387, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1360, in _find_and_load
  File "<frozen importlib._bootstrap>", line 1331, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 935, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 995, in exec_module
  File "<frozen importlib._bootstrap>", line 488, in _call_with_frames_removed
  File "C:\Users\v562455\Downloads\i\prowler\providers\azure\services\keyvault\keyvault_key_expiration_set_in_non_rbac\keyvault_key_expiration_set_in_non_rbac.py", line 2, in <module>
    from prowler.providers.azure.services.keyvault.keyvault_client import keyvault_client
  File "C:\Users\v562455\Downloads\i\prowler\providers\azure\services\keyvault\keyvault_client.py", line 4, in <module>
    keyvault_client = KeyVault(Provider.get_global_provider())
                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\prowler\providers\azure\services\keyvault\keyvault_service.py", line 24, in __init__
    self.key_vaults = self._get_key_vaults(provider)
                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\prowler\providers\azure\services\keyvault\keyvault_service.py", line 42, in _get_key_vaults
    secrets = self._get_secrets(
              ^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\prowler\providers\azure\services\keyvault\keyvault_service.py", line 112, in _get_secrets
    for secret in secrets_list:
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\paging.py", line 123, in __next__
    return next(self._page_iterator)
           ^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\paging.py", line 75, in __next__
    self._response = self._get_next(self.continuation_token)
                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\mgmt\keyvault\v2023_07_01\operations\_secrets_operations.py", line 639, in get_next
    pipeline_response: PipelineResponse = self._client._pipeline.run(  # pylint: disable=protected-access
                                          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\_base.py", line 229, in run
    return first_node.send(pipeline_request)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\_base.py", line 86, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\_base.py", line 86, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\_base.py", line 86, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  [Previous line repeated 2 more times]
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\mgmt\core\policies\_base.py", line 46, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\policies\_redirect.py", line 197, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\policies\_retry.py", line 532, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\policies\_authentication.py", line 147, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\_base.py", line 86, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\_base.py", line 86, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\_base.py", line 86, in send
    response = self.next.send(request)
               ^^^^^^^^^^^^^^^^^^^^^^^
  [Previous line repeated 2 more times]
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\_base.py", line 118, in send
    self._sender.send(request.http_request, **request.context.options),
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\azure\core\pipeline\transport\_requests_basic.py", line 355, in send
    response = self.session.request(  # type: ignore
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\requests\sessions.py", line 589, in request
    resp = self.send(prep, **send_kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\requests\sessions.py", line 703, in send
    r = adapter.send(request, **kwargs)
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\requests\adapters.py", line 667, in send
    resp = conn.urlopen(
           ^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\urllib3\connectionpool.py", line 789, in urlopen
    response = self._make_request(
               ^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\urllib3\connectionpool.py", line 536, in _make_request
    response = conn.getresponse()
               ^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\urllib3\connection.py", line 507, in getresponse
    httplib_response = super().getresponse()
                       ^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\AppData\Local\Programs\Python\Python312\Lib\http\client.py", line 1428, in getresponse
    response.begin()
  File "C:\Users\v562455\AppData\Local\Programs\Python\Python312\Lib\http\client.py", line 331, in begin
    version, status, reason = self._read_status()
                              ^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\AppData\Local\Programs\Python\Python312\Lib\http\client.py", line 292, in _read_status
    line = str(self.fp.readline(_MAXLINE + 1), "iso-8859-1")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\AppData\Local\Programs\Python\Python312\Lib\socket.py", line 707, in readinto
    return self._sock.recv_into(b)
           ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\AppData\Local\Programs\Python\Python312\Lib\ssl.py", line 1252, in recv_into
    return self.read(nbytes, buffer)
           ^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\AppData\Local\Programs\Python\Python312\Lib\ssl.py", line 1104, in read
    return self._sslobj.read(len, buffer)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
KeyboardInterrupt

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "C:\Users\v562455\Downloads\i\prowler.py", line 7, in <module>
    sys.exit(prowler())
             ^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\prowler\__main__.py", line 269, in prowler
    findings = execute_checks(
               ^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\prowler\lib\check\check.py", line 523, in execute_checks
    with alive_bar(
  File "C:\Users\v562455\AppData\Local\Programs\Python\Python312\Lib\contextlib.py", line 158, in __exit__
    self.gen.throw(value)
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\alive_progress\core\progress.py", line 364, in __alive_bar
    alive_repr()
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\alive_progress\core\progress.py", line 165, in alive_repr
    run.last_len = print_cells(fragments, term.cols(), term, run.last_len)
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\v562455\Downloads\i\venv\Lib\site-packages\alive_progress\utils\cells.py", line 109, in print_cells
    term.write(join_cells(fragment))
  File "C:\Users\v562455\AppData\Local\Programs\Python\Python312\Lib\encodings\cp1252.py", line 19, in encode
    return codecs.charmap_encode(input,self.errors,encoding_table)[0]
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
UnicodeEncodeError: 'charmap' codec can't encode characters in position 1-18: character maps to <undefined>
(venv)
