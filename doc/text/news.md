# NEWS

## 0.1.9 - 2015-09-04

### Improvements

  * {Groonga::Client::ScriptSyntax#format_string}: Added a method that
    formats the given Ruby `String` as string
    [in Groonga's script syntax](http://groonga.org/docs/reference/grn_expr/script_syntax.html#string).

## 0.1.8 - 2015-08-08

### Improvements

  * `load`: Supported `Array` as `values` value.

## 0.1.7 - 2015-07-08

### Improvements

  * select: Avoided response value isn't accessible by response column
    name duplication. Data access key for duplicated column name has
    `2`, `3`, ... suffix such as `html_escape2` and `html_escape3`.
    [groonga-dev,03348][Reported by Hiroyuki Sato]

### Thanks

  * Hiroyuki Sato

## 0.1.6 - 2015-06-10

### Fixes

  * Re-added required file.

## 0.1.5 - 2015-06-10

### Fixes

  * Removed `require` for nonexistent file.

## 0.1.4 - 2015-06-10

### Changes

  * Moved `groonga-client` command to groonga-client-cli gem.
    It's an incompatible change.

## 0.1.3 - 2015-05-25

### Improvements

  * Stopped to use yajl-ruby.

## 0.1.2 - 2015-05-13

### Improvements

  * groonga-client: Supported split load.
  * groonga-client: Added `--read-timeout` option.

## 0.1.1 - 2015-04-20

### Improvements

  * groonga-client: Added a command that sends Groonga commands to a
    Groonga server.

## 0.1.0 - 2014-11-05

### Improvements

  * response: Added {Groonga::Client::Response::Error#message}.
  * response: Added {Groonga::Client::Response::Base#status_code}.
  * response: Added {Groonga::Client::Response::Base#start_time}.
  * response: Added {Groonga::Client::Response::Base#elapsed_time}.
  * response: Added {Groonga::Client::Response::Base#success?}.

## 0.0.9 - 2014-09-30

### Improvements

  * HTTP: Supported "load" by POST.
  * HTTP: Added synchronous backend.

## 0.0.8 - 2014-05-12

### Improvements

  * HTTP, Thread: Supported "bad request" response.
  * HTTP, Thread: Supported JSON body in "internal server error" response.

## 0.0.7 - 2014-03-28

### Improvements

  * Supported error response.

## 0.0.6 - 2014-03-25

### Fixes

  * HTTP, Cool.io: Fixed a bug that body is handled when body is
    partially read.

## 0.0.5 - 2014-03-25

### Improvements

  * Wrapped internal connection errors by
    `Groonga::Client::Connection::Error`.
  * Supported asynchronous request by calling with block.
  * Added Cool.io HTTP backend.

### Changes

  * Changed protocol implementation module/directory name to
    `protocol` from `connection`.

### Fixes

  * Fixed a bug that options passed to `Groonga::Client.new` is
    changed destructively.

## 0.0.4 - 2013-10-29

### Improvements

  * http: Supported timeout error.
  * status: Added {Groonga::Client::Response::Status#alloc_count} and
    {Groonga::Client::Response::Status#n_allocations}.

## 0.0.3 - 2013-09-18

### Improvements

  * Supported "table_create" command.
  * {Groonga::Client.open} returns block value.
  * Supported {Groonga::Client#close}.
  * select: Supported auto time value conversion.
  * select: Renamed to {Groonga::Client::Response::Select#n_hits}
    from #n_records. It is a backward incompatible change.
  * Added {Groonga::Client::Connection::Error} as an abstracted error.
  * Required groonga-command 1.0.4 or later.

## 0.0.2 - 2013-07-08

### Improvements

  * Supported "select" command.
  * Supported Enumerable type interface in
    Response::TableList and Response::ColumnList

## 0.0.1 - 2013-06-27

Initial release!!!
