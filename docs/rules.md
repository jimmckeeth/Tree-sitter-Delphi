# Tree-sitter Delphi Rules List

## <a id="summary"></a>Summary

| Category | Rules | Tested | Untested | Total Tests | Passing | Failing |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| [Declarations & Definitions](#declarations-definitions) | 51 | 41 | 10 | 194 | 110 | 0 |
| [Expressions](#expressions) | 12 | 10 | 2 | 150 | 88 | 0 |
| [High-Level Structure](#high-level-structure) | 9 | 9 | 0 | 186 | 106 | 0 |
| [Internal Helpers](#internal-helpers) | 26 | 0 | 26 | 0 | 0 | 0 |
| [Keywords & Terminals](#keywords-terminals) | 161 | 109 | 52 | 194 | 110 | 0 |
| [Literals](#literals) | 7 | 6 | 1 | 102 | 50 | 0 |
| [Other](#other) | 12 | 5 | 7 | 194 | 110 | 0 |
| [Statements](#statements) | 24 | 23 | 1 | 174 | 101 | 0 |
| **TOTAL** | **302** | **203** | **99** | **1194** | **675** | **0** |

---

## <a id="declarations-definitions"></a>Declarations & Definitions

| Rule Name | Tested In |
| :--- | :--- |
| **declArg** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `pascocoa.txt`, `preprocessor.txt`, `routines.txt` |
| **declArgs** | `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `pascocoa.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **declArray** | `declarations.txt`, `literals.txt` |
| **declClass** | `attributes.txt`, `declarations.txt`, `modules.txt`, `pascocoa.txt` |
| **declConst** | `declarations.txt`, `literals.txt`, `routines.txt` |
| **declConsts** | `declarations.txt`, `literals.txt`, `routines.txt` |
| **declEnum** | `attributes.txt`, `declarations.txt` |
| **declEnumValue** | `attributes.txt`, `declarations.txt` |
| **declExport** | *No explicit test found* |
| **declExports** | *No explicit test found* |
| **declField** | `declarations.txt`, `pascocoa.txt` |
| **declFile** | `declarations.txt` |
| **declHelper** | *No explicit test found* |
| **declIntf** | `attributes.txt`, `declarations.txt` |
| **declLabel** | *No explicit test found* |
| **declLabels** | *No explicit test found* |
| **declMetaClass** | `declarations.txt` |
| **declProc** | `attributes.txt`, `declarations.txt`, `expressions.txt`, `generics-fpc.txt`, `lambdas.txt`, `modern_delphi.txt`, `modules.txt`, `pascocoa.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **declProcFwd** | *No explicit test found* |
| **declProcRef** | `declarations.txt`, `lambdas.txt` |
| **declProp** | `attributes.txt`, `declarations.txt` |
| **declPropArgs** | `attributes.txt`, `declarations.txt` |
| **declSection** | `declarations.txt`, `pascocoa.txt` |
| **declSet** | `declarations.txt` |
| **declString** | `declarations.txt`, `modern_delphi.txt` |
| **declType** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `modules.txt`, `pascocoa.txt`, `routines.txt` |
| **declTypes** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `modules.txt`, `pascocoa.txt`, `routines.txt` |
| **declUses** | `modules.txt` |
| **declVar** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `modern_delphi.txt`, `preprocessor.txt`, `routines.txt` |
| **declVariant** | `declarations.txt` |
| **declVariantClause** | `declarations.txt` |
| **declVariantField** | *No explicit test found* |
| **declVars** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `modern_delphi.txt`, `preprocessor.txt`, `routines.txt` |
| **defProc** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `modern_delphi.txt`, `modules.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **defaultValue** | `declarations.txt`, `literals.txt`, `modern_delphi.txt`, `routines.txt` |
| **genericArg** | `generics-delphi.txt`, `generics-fpc.txt` |
| **genericArgs** | `generics-delphi.txt`, `generics-fpc.txt` |
| **genericDot** | `generics-delphi.txt`, `generics-fpc.txt`, `modules.txt`, `routines.txt` |
| **genericTpl** | `generics-delphi.txt`, `generics-fpc.txt` |
| **guid** | `attributes.txt`, `declarations.txt` |
| **operatorDot** | *No explicit test found* |
| **operatorName** | `declarations.txt`, `routines.txt` |
| **procAttribute** | `attributes.txt`, `declarations.txt`, `pascocoa.txt` |
| **procExternal** | `attributes.txt` |
| **rttiAttributes** | `attributes.txt` |
| **type** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `literals.txt`, `modules.txt`, `pascocoa.txt`, `preprocessor.txt`, `routines.txt` |
| **typeref** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `inlinevar.txt`, `lambdas.txt`, `literals.txt`, `modules.txt`, `pascocoa.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **typerefArgs** | `generics-delphi.txt`, `generics-fpc.txt` |
| **typerefDot** | *No explicit test found* |
| **typerefPtr** | *No explicit test found* |
| **typerefTpl** | `generics-delphi.txt`, `generics-fpc.txt` |

[Back to Summary](#summary)

## <a id="expressions"></a>Expressions

| Rule Name | Tested In |
| :--- | :--- |
| **exprArgs** | `attributes.txt`, `expressions.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `modern_delphi.txt`, `preprocessor.txt` |
| **exprAs** | *No explicit test found* |
| **exprBinary** | `expressions.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `literals.txt` |
| **exprBrackets** | `expressions.txt`, `literals.txt` |
| **exprCall** | `attributes.txt`, `expressions.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `modern_delphi.txt`, `preprocessor.txt` |
| **exprDeref** | *No explicit test found* |
| **exprDot** | `expressions.txt`, `modern_delphi.txt` |
| **exprParens** | `expressions.txt`, `lambdas.txt` |
| **exprSubscript** | `expressions.txt` |
| **exprTpl** | `generics-delphi.txt`, `generics-fpc.txt`, `modern_delphi.txt` |
| **exprUnary** | `expressions.txt` |
| **range** | `declarations.txt`, `expressions.txt`, `literals.txt`, `statements.txt` |

[Back to Summary](#summary)

## <a id="high-level-structure"></a>High-Level Structure

| Rule Name | Tested In |
| :--- | :--- |
| **finalization** | `modules.txt` |
| **implementation** | `modules.txt` |
| **initialization** | `modules.txt` |
| **interface** | `modules.txt` |
| **library** | `modules.txt` |
| **moduleName** | `modules.txt` |
| **program** | `modules.txt` |
| **root** | `attributes.txt`, `declarations.txt`, `expressions.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `literals.txt`, `modern_delphi.txt`, `modules.txt`, `pascocoa.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **unit** | `modules.txt` |

[Back to Summary](#summary)

## <a id="internal-helpers"></a>Internal Helpers

| Rule Name | Tested In |
| :--- | :--- |
| **_classDeclarations** | *No explicit test found* |
| **_declClass** | *No explicit test found* |
| **_declFields** | *No explicit test found* |
| **_declOperator** | *No explicit test found* |
| **_declProc** | *No explicit test found* |
| **_declarations** | *No explicit test found* |
| **_definition** | *No explicit test found* |
| **_definitions** | *No explicit test found* |
| **_exceptionHandlers** | *No explicit test found* |
| **_expr** | *No explicit test found* |
| **_genericName** | *No explicit test found* |
| **_initializer** | *No explicit test found* |
| **_literal** | *No explicit test found* |
| **_literalFloat** | *No explicit test found* |
| **_literalInt** | *No explicit test found* |
| **_literalString** | *No explicit test found* |
| **_operatorName** | *No explicit test found* |
| **_procAttribute** | *No explicit test found* |
| **_procAttributeNoExt** | *No explicit test found* |
| **_ref** | *No explicit test found* |
| **_space** | *No explicit test found* |
| **_statement** | *No explicit test found* |
| **_statements** | *No explicit test found* |
| **_statementsTr** | *No explicit test found* |
| **_typeref** | *No explicit test found* |
| **_visibility** | *No explicit test found* |

[Back to Summary](#summary)

## <a id="keywords-terminals"></a>Keywords & Terminals

| Rule Name | Tested In |
| :--- | :--- |
| **kAbsolute** | *No explicit test found* |
| **kAbstract** | `attributes.txt` |
| **kAdd** | `declarations.txt`, `literals.txt`, `routines.txt` |
| **kAlias** | `attributes.txt` |
| **kAnd** | `expressions.txt` |
| **kArray** | `declarations.txt`, `literals.txt` |
| **kAs** | `expressions.txt` |
| **kAsm** | `statements.txt` |
| **kAssembler** | *No explicit test found* |
| **kAssign** | `inlinevar.txt`, `lambdas.txt`, `modern_delphi.txt`, `statements.txt` |
| **kAssignAdd** | *No explicit test found* |
| **kAssignDiv** | *No explicit test found* |
| **kAssignMul** | *No explicit test found* |
| **kAssignSub** | *No explicit test found* |
| **kAt** | `expressions.txt` |
| **kBegin** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `modern_delphi.txt`, `modules.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **kCase** | `declarations.txt`, `modern_delphi.txt`, `statements.txt` |
| **kCdecl** | `attributes.txt` |
| **kClass** | `attributes.txt`, `declarations.txt`, `modules.txt`, `pascocoa.txt` |
| **kConst** | `declarations.txt`, `literals.txt`, `modern_delphi.txt`, `routines.txt` |
| **kConstref** | *No explicit test found* |
| **kConstructor** | `declarations.txt`, `routines.txt` |
| **kCppdecl** | *No explicit test found* |
| **kCvar** | `attributes.txt` |
| **kDefault** | `attributes.txt`, `declarations.txt` |
| **kDelayed** | *No explicit test found* |
| **kDeprecated** | *No explicit test found* |
| **kDestructor** | `declarations.txt`, `routines.txt` |
| **kDispId** | *No explicit test found* |
| **kDispInterface** | *No explicit test found* |
| **kDiv** | `expressions.txt` |
| **kDo** | `inlinevar.txt`, `modern_delphi.txt`, `preprocessor.txt`, `statements.txt` |
| **kDot** | `expressions.txt`, `generics-fpc.txt`, `modern_delphi.txt`, `modules.txt`, `routines.txt` |
| **kDownto** | `statements.txt` |
| **kDynamic** | *No explicit test found* |
| **kElse** | `statements.txt` |
| **kEnd** | `attributes.txt`, `declarations.txt`, `expressions.txt`, `generics-fpc.txt`, `lambdas.txt`, `modern_delphi.txt`, `modules.txt`, `pascocoa.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **kEndDot** | `modules.txt` |
| **kEndif** | *No explicit test found* |
| **kEq** | `attributes.txt`, `declarations.txt`, `expressions.txt`, `generics-fpc.txt`, `lambdas.txt`, `literals.txt`, `modules.txt`, `pascocoa.txt`, `routines.txt` |
| **kExcept** | `statements.txt` |
| **kExperimental** | *No explicit test found* |
| **kExport** | *No explicit test found* |
| **kExports** | *No explicit test found* |
| **kExternal** | `attributes.txt`, `pascocoa.txt` |
| **kFalse** | *No explicit test found* |
| **kFar** | *No explicit test found* |
| **kFdiv** | `expressions.txt` |
| **kFile** | `declarations.txt` |
| **kFinalization** | `modules.txt` |
| **kFinally** | `statements.txt` |
| **kFor** | `inlinevar.txt`, `modern_delphi.txt`, `statements.txt` |
| **kForward** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `modules.txt` |
| **kFunction** | `declarations.txt`, `lambdas.txt`, `modules.txt`, `pascocoa.txt`, `routines.txt` |
| **kGeneric** | `generics-fpc.txt` |
| **kGoto** | `statements.txt` |
| **kGt** | `expressions.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `modern_delphi.txt` |
| **kGte** | `expressions.txt` |
| **kHardfloat** | *No explicit test found* |
| **kHat** | `expressions.txt` |
| **kHelper** | *No explicit test found* |
| **kIf** | `generics-delphi.txt`, `generics-fpc.txt`, `preprocessor.txt`, `statements.txt` |
| **kIfdef** | *No explicit test found* |
| **kIfndef** | *No explicit test found* |
| **kImplementation** | `modules.txt` |
| **kImplements** | *No explicit test found* |
| **kIn** | `expressions.txt`, `modern_delphi.txt`, `statements.txt` |
| **kIndex** | `attributes.txt`, `declarations.txt` |
| **kInherited** | *No explicit test found* |
| **kInitialization** | `modules.txt` |
| **kInline** | `attributes.txt` |
| **kInterface** | `attributes.txt`, `declarations.txt`, `modules.txt` |
| **kInterrupt** | *No explicit test found* |
| **kIocheck** | *No explicit test found* |
| **kIs** | `expressions.txt` |
| **kLabel** | *No explicit test found* |
| **kLibrary** | `modules.txt` |
| **kLocal** | *No explicit test found* |
| **kLt** | `expressions.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `modern_delphi.txt` |
| **kLte** | `expressions.txt` |
| **kMessage** | `attributes.txt`, `pascocoa.txt` |
| **kMod** | `expressions.txt` |
| **kMs_abi_cdecl** | *No explicit test found* |
| **kMs_abi_default** | *No explicit test found* |
| **kMul** | `expressions.txt` |
| **kMwpascal** | *No explicit test found* |
| **kName** | `attributes.txt` |
| **kNear** | *No explicit test found* |
| **kNeq** | `expressions.txt` |
| **kNil** | *No explicit test found* |
| **kNodefault** | *No explicit test found* |
| **kNoreturn** | *No explicit test found* |
| **kNostackframe** | *No explicit test found* |
| **kNot** | `expressions.txt` |
| **kObjccategory** | `pascocoa.txt` |
| **kObjcclass** | `pascocoa.txt` |
| **kObjcprotocol** | `pascocoa.txt` |
| **kObject** | `declarations.txt` |
| **kOf** | `declarations.txt`, `literals.txt`, `modern_delphi.txt`, `statements.txt` |
| **kOn** | `statements.txt` |
| **kOperator** | `declarations.txt`, `routines.txt` |
| **kOptional** | `pascocoa.txt` |
| **kOr** | `expressions.txt` |
| **kOtherwise** | `modern_delphi.txt` |
| **kOut** | `routines.txt` |
| **kOverload** | *No explicit test found* |
| **kOverride** | `attributes.txt`, `pascocoa.txt` |
| **kPacked** | *No explicit test found* |
| **kPascal** | `attributes.txt` |
| **kPlatform** | *No explicit test found* |
| **kPrivate** | `declarations.txt`, `pascocoa.txt` |
| **kProcedure** | `attributes.txt`, `declarations.txt`, `expressions.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `modern_delphi.txt`, `modules.txt`, `pascocoa.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **kProgram** | `modules.txt` |
| **kProperty** | `attributes.txt`, `declarations.txt` |
| **kProtected** | `declarations.txt` |
| **kPublic** | `attributes.txt`, `declarations.txt`, `pascocoa.txt` |
| **kPublished** | `declarations.txt` |
| **kRaise** | `statements.txt` |
| **kRead** | `attributes.txt`, `declarations.txt` |
| **kRecord** | `declarations.txt` |
| **kReference** | `lambdas.txt` |
| **kRegister** | `attributes.txt` |
| **kReintroduce** | `pascocoa.txt` |
| **kRepeat** | `statements.txt` |
| **kRequired** | `pascocoa.txt` |
| **kResourcestring** | `declarations.txt` |
| **kSafecall** | *No explicit test found* |
| **kSaveregisters** | *No explicit test found* |
| **kSealed** | *No explicit test found* |
| **kSet** | `declarations.txt` |
| **kShl** | `expressions.txt` |
| **kShr** | `expressions.txt` |
| **kSoftfloat** | *No explicit test found* |
| **kSpecialize** | `generics-fpc.txt` |
| **kStatic** | *No explicit test found* |
| **kStdcall** | `attributes.txt` |
| **kStored** | `declarations.txt` |
| **kStrict** | `declarations.txt` |
| **kString** | `declarations.txt`, `modern_delphi.txt` |
| **kSub** | `expressions.txt` |
| **kSysv_abi_cdecl** | *No explicit test found* |
| **kSysv_abi_default** | *No explicit test found* |
| **kThen** | `generics-delphi.txt`, `generics-fpc.txt`, `preprocessor.txt`, `statements.txt` |
| **kThreadvar** | *No explicit test found* |
| **kTo** | `inlinevar.txt`, `lambdas.txt`, `statements.txt` |
| **kTrue** | `preprocessor.txt` |
| **kTry** | `statements.txt` |
| **kType** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `modules.txt`, `pascocoa.txt`, `routines.txt` |
| **kUnimplemented** | *No explicit test found* |
| **kUnit** | `modules.txt` |
| **kUntil** | `statements.txt` |
| **kUses** | `modules.txt` |
| **kVar** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `modern_delphi.txt`, `preprocessor.txt`, `routines.txt` |
| **kVarargs** | *No explicit test found* |
| **kVectorcall** | *No explicit test found* |
| **kVirtual** | `attributes.txt` |
| **kWhile** | `preprocessor.txt`, `statements.txt` |
| **kWinapi** | *No explicit test found* |
| **kWith** | `statements.txt` |
| **kWrite** | `declarations.txt` |
| **kXor** | `expressions.txt` |

[Back to Summary](#summary)

## <a id="literals"></a>Literals

| Rule Name | Tested In |
| :--- | :--- |
| **arrInitializer** | `literals.txt` |
| **literalChar** | *No explicit test found* |
| **literalNumber** | `attributes.txt`, `declarations.txt`, `inlinevar.txt`, `lambdas.txt`, `literals.txt`, `modern_delphi.txt` |
| **literalString** | `attributes.txt`, `declarations.txt`, `literals.txt`, `modern_delphi.txt`, `pascocoa.txt`, `preprocessor.txt` |
| **literalStringMultiline** | `modern_delphi.txt` |
| **recInitializer** | `literals.txt` |
| **recInitializerField** | `literals.txt` |

[Back to Summary](#summary)

## <a id="other"></a>Other

| Rule Name | Tested In |
| :--- | :--- |
| **asmBody** | *No explicit test found* |
| **comment** | `preprocessor.txt` |
| **conflicts** | *No explicit test found* |
| **extras** | *No explicit test found* |
| **identifier** | `attributes.txt`, `declarations.txt`, `expressions.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `inlinevar.txt`, `lambdas.txt`, `literals.txt`, `modern_delphi.txt`, `modules.txt`, `pascocoa.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **ifElse** | `statements.txt` |
| **inherited** | *No explicit test found* |
| **lambda** | `inlinevar.txt` |
| **legacyFormat** | *No explicit test found* |
| **nestedIf** | *No explicit test found* |
| **pp** | `preprocessor.txt` |
| **word** | *No explicit test found* |

[Back to Summary](#summary)

## <a id="statements"></a>Statements

| Rule Name | Tested In |
| :--- | :--- |
| **asm** | `statements.txt` |
| **assignment** | `inlinevar.txt`, `lambdas.txt`, `modern_delphi.txt`, `statements.txt` |
| **block** | `attributes.txt`, `declarations.txt`, `generics-delphi.txt`, `generics-fpc.txt`, `lambdas.txt`, `modern_delphi.txt`, `modules.txt`, `preprocessor.txt`, `routines.txt`, `statements.txt` |
| **case** | `declarations.txt`, `modern_delphi.txt`, `statements.txt` |
| **caseCase** | `modern_delphi.txt`, `statements.txt` |
| **caseLabel** | `declarations.txt`, `modern_delphi.txt`, `statements.txt` |
| **exceptionElse** | `statements.txt` |
| **exceptionHandler** | `statements.txt` |
| **for** | `inlinevar.txt`, `statements.txt` |
| **foreach** | `modern_delphi.txt`, `statements.txt` |
| **goto** | `statements.txt` |
| **if** | `generics-delphi.txt`, `generics-fpc.txt`, `preprocessor.txt`, `statements.txt` |
| **inlineConst** | `modern_delphi.txt` |
| **label** | `statements.txt` |
| **raise** | `statements.txt` |
| **repeat** | `statements.txt` |
| **statement** | `expressions.txt`, `generics-fpc.txt`, `modern_delphi.txt`, `modules.txt`, `preprocessor.txt`, `statements.txt` |
| **statements** | `statements.txt` |
| **statementsTr** | *No explicit test found* |
| **try** | `statements.txt` |
| **varAssignDef** | `inlinevar.txt`, `modern_delphi.txt` |
| **varDef** | `inlinevar.txt` |
| **while** | `preprocessor.txt`, `statements.txt` |
| **with** | `statements.txt` |

[Back to Summary](#summary)

