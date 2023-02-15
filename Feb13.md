## Ans 1
We have to use the Exception class while creating a Custom Exception because a custom error class could logs errors, inspect an object but it is up to us what the exception class does, although a custom class will not usually do a great deal more than display a message.

## Ans 2


```python
import inspect
def treeClass(cls, ind = 0):
    print ('-' * ind, cls.__name__)
    for i in cls.__subclasses__():
        treeClass(i, ind + 3)

print("Hierarchy for Built-in exceptions is : ")
inspect.getclasstree(inspect.getmro(BaseException))
treeClass(BaseException)
```

    Hierarchy for Built-in exceptions is : 
     BaseException
    --- Exception
    ------ TypeError
    --------- FloatOperation
    --------- MultipartConversionError
    ------ StopAsyncIteration
    ------ StopIteration
    ------ ImportError
    --------- ModuleNotFoundError
    --------- ZipImportError
    ------ OSError
    --------- ConnectionError
    ------------ BrokenPipeError
    ------------ ConnectionAbortedError
    ------------ ConnectionRefusedError
    ------------ ConnectionResetError
    --------------- RemoteDisconnected
    --------- BlockingIOError
    --------- ChildProcessError
    --------- FileExistsError
    --------- FileNotFoundError
    --------- IsADirectoryError
    --------- NotADirectoryError
    --------- InterruptedError
    ------------ InterruptedSystemCall
    --------- PermissionError
    --------- ProcessLookupError
    --------- TimeoutError
    --------- UnsupportedOperation
    --------- itimer_error
    --------- herror
    --------- gaierror
    --------- SSLError
    ------------ SSLCertVerificationError
    ------------ SSLZeroReturnError
    ------------ SSLWantWriteError
    ------------ SSLWantReadError
    ------------ SSLSyscallError
    ------------ SSLEOFError
    --------- Error
    ------------ SameFileError
    --------- SpecialFileError
    --------- ExecError
    --------- ReadError
    --------- URLError
    ------------ HTTPError
    ------------ ContentTooShortError
    --------- BadGzipFile
    ------ EOFError
    --------- IncompleteReadError
    ------ RuntimeError
    --------- RecursionError
    --------- NotImplementedError
    ------------ ZMQVersionError
    ------------ StdinNotImplementedError
    --------- _DeadlockError
    --------- BrokenBarrierError
    --------- BrokenExecutor
    ------------ BrokenThreadPool
    --------- SendfileNotAvailableError
    --------- ExtractionError
    --------- VariableError
    ------ NameError
    --------- UnboundLocalError
    ------ AttributeError
    --------- FrozenInstanceError
    ------ SyntaxError
    --------- IndentationError
    ------------ TabError
    ------ LookupError
    --------- IndexError
    --------- KeyError
    ------------ NoSuchKernel
    ------------ UnknownBackend
    --------- CodecRegistryError
    ------ ValueError
    --------- UnicodeError
    ------------ UnicodeEncodeError
    ------------ UnicodeDecodeError
    ------------ UnicodeTranslateError
    --------- UnsupportedOperation
    --------- JSONDecodeError
    --------- SSLCertVerificationError
    --------- Error
    --------- UnsupportedDigestmodError
    --------- IllegalMonthError
    --------- IllegalWeekdayError
    --------- ParserError
    --------- ClassNotFound
    --------- ClipboardEmpty
    --------- MessageDefect
    ------------ NoBoundaryInMultipartDefect
    ------------ StartBoundaryNotFoundDefect
    ------------ CloseBoundaryNotFoundDefect
    ------------ FirstHeaderLineIsContinuationDefect
    ------------ MisplacedEnvelopeHeaderDefect
    ------------ MissingHeaderBodySeparatorDefect
    ------------ MultipartInvariantViolationDefect
    ------------ InvalidMultipartContentTransferEncodingDefect
    ------------ UndecodableBytesDefect
    ------------ InvalidBase64PaddingDefect
    ------------ InvalidBase64CharactersDefect
    ------------ InvalidBase64LengthDefect
    ------------ HeaderDefect
    --------------- InvalidHeaderDefect
    --------------- HeaderMissingRequiredValue
    --------------- NonPrintableDefect
    --------------- ObsoleteHeaderDefect
    --------------- NonASCIILocalPartDefect
    --------------- InvalidDateDefect
    --------- MacroToEdit
    --------- InvalidFileException
    --------- UnequalIterablesError
    --------- InvalidVersion
    --------- _InvalidELFFileHeader
    --------- InvalidWheelFilename
    --------- InvalidSdistFilename
    --------- InvalidSpecifier
    --------- InvalidMarker
    --------- UndefinedComparison
    --------- UndefinedEnvironmentName
    --------- InvalidRequirement
    ------------ RequirementParseError
    --------- InvalidVersion
    ------ AssertionError
    ------ ArithmeticError
    --------- FloatingPointError
    --------- OverflowError
    --------- ZeroDivisionError
    ------------ DivisionByZero
    ------------ DivisionUndefined
    --------- DecimalException
    ------------ Clamped
    ------------ Rounded
    --------------- Underflow
    --------------- Overflow
    ------------ Inexact
    --------------- Underflow
    --------------- Overflow
    ------------ Subnormal
    --------------- Underflow
    ------------ DivisionByZero
    ------------ FloatOperation
    ------------ InvalidOperation
    --------------- ConversionSyntax
    --------------- DivisionImpossible
    --------------- DivisionUndefined
    --------------- InvalidContext
    ------ SystemError
    --------- CodecRegistryError
    ------ ReferenceError
    ------ MemoryError
    ------ BufferError
    ------ Warning
    --------- UserWarning
    ------------ GetPassWarning
    ------------ FormatterWarning
    --------- EncodingWarning
    --------- DeprecationWarning
    ------------ ProvisionalWarning
    --------- PendingDeprecationWarning
    --------- SyntaxWarning
    --------- RuntimeWarning
    ------------ ProactorSelectorThreadWarning
    ------------ UnknownTimezoneWarning
    ------------ PEP440Warning
    --------- FutureWarning
    ------------ ProvisionalCompleterWarning
    --------- ImportWarning
    --------- UnicodeWarning
    --------- BytesWarning
    --------- ResourceWarning
    --------- DeprecatedTzFormatWarning
    --------- PkgResourcesDeprecationWarning
    ------ _OptionError
    ------ _Error
    ------ error
    ------ Verbose
    ------ Error
    ------ SubprocessError
    --------- CalledProcessError
    --------- TimeoutExpired
    ------ TokenError
    ------ StopTokenizing
    ------ ClassFoundException
    ------ EndOfBlock
    ------ TraitError
    ------ Error
    ------ Error
    --------- CancelledError
    --------- TimeoutError
    --------- InvalidStateError
    ------ _GiveupOnSendfile
    ------ error
    ------ Incomplete
    ------ TimeoutError
    ------ InvalidStateError
    ------ LimitOverrunError
    ------ QueueEmpty
    ------ QueueFull
    ------ Empty
    ------ Full
    ------ ArgumentError
    ------ ZMQBaseError
    --------- ZMQError
    ------------ ContextTerminated
    ------------ Again
    ------------ InterruptedSystemCall
    --------- ZMQBindError
    --------- NotDone
    ------ PickleError
    --------- PicklingError
    --------- UnpicklingError
    ------ _Stop
    ------ ArgumentError
    ------ ArgumentTypeError
    ------ ConfigError
    --------- ConfigLoaderError
    ------------ ArgumentError
    --------- ConfigFileNotFound
    ------ ConfigurableError
    --------- MultipleInstanceError
    ------ ApplicationError
    ------ error
    ------ TimeoutError
    ------ error
    ------ ReturnValueIgnoredError
    ------ KeyReuseError
    ------ UnknownKeyError
    ------ LeakedCallbackError
    ------ BadYieldError
    ------ ReturnValueIgnoredError
    ------ Return
    ------ InvalidPortNumber
    ------ error
    ------ LZMAError
    ------ RegistryError
    ------ _GiveupOnFastCopy
    ------ Error
    --------- NoSectionError
    --------- DuplicateSectionError
    --------- DuplicateOptionError
    --------- NoOptionError
    --------- InterpolationError
    ------------ InterpolationMissingOptionError
    ------------ InterpolationSyntaxError
    ------------ InterpolationDepthError
    --------- ParsingError
    ------------ MissingSectionHeaderError
    ------ NoIPAddresses
    ------ BadZipFile
    ------ LargeZipFile
    ------ BadEntryPoint
    ------ NoSuchEntryPoint
    ------ DuplicateKernelError
    ------ ErrorDuringImport
    ------ NotOneValueFound
    ------ CannotEval
    ------ OptionError
    ------ BdbQuit
    ------ Restart
    ------ ExceptionPexpect
    --------- EOF
    --------- TIMEOUT
    ------ PtyProcessError
    ------ FindCmdError
    ------ HomeDirError
    ------ ProfileDirError
    ------ IPythonCoreError
    --------- TryNext
    --------- UsageError
    --------- StdinNotImplementedError
    ------ InputRejected
    ------ GetoptError
    ------ ErrorToken
    ------ PrefilterError
    ------ AliasError
    --------- InvalidAliasError
    ------ Error
    --------- InterfaceError
    --------- DatabaseError
    ------------ InternalError
    ------------ OperationalError
    ------------ ProgrammingError
    ------------ IntegrityError
    ------------ DataError
    ------------ NotSupportedError
    ------ Warning
    ------ SpaceInInput
    ------ DOMException
    --------- IndexSizeErr
    --------- DomstringSizeErr
    --------- HierarchyRequestErr
    --------- WrongDocumentErr
    --------- InvalidCharacterErr
    --------- NoDataAllowedErr
    --------- NoModificationAllowedErr
    --------- NotFoundErr
    --------- NotSupportedErr
    --------- InuseAttributeErr
    --------- InvalidStateErr
    --------- SyntaxErr
    --------- InvalidModificationErr
    --------- NamespaceErr
    --------- InvalidAccessErr
    --------- ValidationErr
    ------ ValidationError
    ------ EditReadOnlyBuffer
    ------ _Retry
    ------ InvalidLayoutError
    ------ HeightIsUnknownError
    ------ ParserSyntaxError
    ------ InternalParseError
    ------ _PositionUpdatingFinished
    ------ SimpleGetItemNotFound
    ------ UncaughtAttributeError
    ------ HasNoContext
    ------ ParamIssue
    ------ _JediError
    --------- InternalError
    --------- WrongVersion
    --------- RefactoringError
    ------ OnErrorLeaf
    ------ InvalidPythonEnvironment
    ------ MessageError
    --------- MessageParseError
    ------------ HeaderParseError
    ------------ BoundaryError
    --------- MultipartConversionError
    --------- CharsetError
    ------ Error
    ------ HTTPException
    --------- NotConnected
    --------- InvalidURL
    --------- UnknownProtocol
    --------- UnknownTransferEncoding
    --------- UnimplementedFileMode
    --------- IncompleteRead
    --------- ImproperConnectionState
    ------------ CannotSendRequest
    ------------ CannotSendHeader
    ------------ ResponseNotReady
    --------- BadStatusLine
    ------------ RemoteDisconnected
    --------- LineTooLong
    ------ InteractivelyDefined
    ------ KillEmbedded
    ------ Error
    --------- NoSuchProcess
    ------------ ZombieProcess
    --------- AccessDenied
    --------- TimeoutExpired
    ------ _Ipv6UnsupportedError
    ------ QueueEmpty
    ------ QueueFull
    ------ DebuggerInitializationError
    ------ ExpatError
    ------ Error
    --------- ProtocolError
    --------- ResponseError
    --------- Fault
    ------ ParseBaseException
    --------- ParseException
    --------- ParseFatalException
    ------------ ParseSyntaxException
    ------ RecursiveGrammarException
    ------ ResolutionError
    --------- VersionConflict
    ------------ ContextualVersionConflict
    --------- DistributionNotFound
    --------- UnknownExtra
    ------ _Error
    ------ UnableToResolveVariableException
    ------ InvalidTypeInArgsException
    --- GeneratorExit
    --- SystemExit
    --- KeyboardInterrupt
    --- CancelledError
    --- AbortThread


## Ans 3
This class is the base class for those built-in exceptions that are raised for various arithmetic errors such as :
OverflowError, ZeroDivisionError, FloatingPointError


```python
## zero division error
try:
    1/0
except ArithmeticError as e:
    print(f"{e}")

```

    division by zero



```python
##overflow error
j = 5.0
try:
    for i in range(1, 1000):
        j = j**i
except ArithmeticError as e:
    print(f"{e}")
```

    (34, 'Numerical result out of range')


## Ans 4
LookupError Exception is the Base class for errors raised when something can’t be found. The base class for the exceptions that are raised when a key or index used on a mapping or sequence is invalid: IndexError, KeyError.



```python
## key error exception
info = {'name': 'Pulkit Singhvi',
                'age': 22,
                'course': 'Data Science'}
user_input = input('What do you want to learn about ')

try:
    print(f'{user_input} is {info[user_input]}')
except LookupError as e:
    print(f'{e}, {e.__class__}')
```

    What do you want to learn about  number


    'number', <class 'KeyError'>



```python
## index error
list = ['a', 's', 'd', 'f', 'g']
try:
    print (list[5])
except IndexError as e:
    print (e)
```

    list index out of range


## Ans 5
The ImportError is raised when an import statement has trouble successfully importing the specified module.ModuleNotFoundError occurs when you're trying to access or use a module that cannot be found. Here are a few reasons why a module may not be found:

• The module we tried importing is not installed on our computer

• We spelled a module incorrectly 

• We use an incorrect casing for a module 

• We are importing a module using the wrong path



## Ans 6
Some best practices for exception handling in python are:  
• Use always a specific exception

• Print always a valid msg

• Always try to log

• Always avoid to write a multiple exception handling 

• Cleanup all the resources


```python

```
