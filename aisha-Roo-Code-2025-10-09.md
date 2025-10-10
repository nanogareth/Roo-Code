# Codebase Structure Summary

Total Code Files: 1335
Total Functions: 2221

## Files

### apps\vscode-e2e\src\runTest.ts
**Purpose:** Runs end-to-end tests within a VS Code environment.

**Exported Functions:**
- `main` → `Promise<void>`

**Key Imports:** `path`, `os`, `fs/promises`, `@vscode/test-electron`

---

### apps\vscode-e2e\src\suite\extension.test.ts
**Purpose:** Tests the registration of Roo Code extension commands.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`

**Key Imports:** `assert`, `vscode`, `./test-utils`

---

### apps\vscode-e2e\src\suite\index.ts
**Purpose:** Initializes and runs the Roo Code extension tests.

**Exported Functions:**
- `run` → `Promise<void>`

**Key Imports:** `path`, `mocha`, `glob`, `vscode`, `@roo-code/types`, `./utils`

---

### apps\vscode-e2e\src\suite\markdown-lists.test.ts
**Purpose:** Verifies the correct rendering of markdown lists in chat messages.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`

**Key Imports:** `assert`, `@roo-code/types`, `./utils`, `./test-utils`

---

### apps\vscode-e2e\src\suite\modes.test.ts
**Purpose:** Tests the switching of Roo Code modes functionality.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`

**Key Imports:** `assert`, `@roo-code/types`, `./utils`, `./test-utils`

---

### apps\vscode-e2e\src\suite\subtasks.test.ts
**Purpose:** Tests the handling of subtask cancellation and resumption.

**Key Imports:** `assert`, `@roo-code/types`, `./utils`

---

### apps\vscode-e2e\src\suite\task.test.ts
**Purpose:** Tests the prompt and response handling of Roo Code tasks.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`

**Key Imports:** `assert`, `@roo-code/types`, `./utils`, `./test-utils`

---

### apps\vscode-e2e\src\suite\test-utils.ts
**Purpose:** Provides utility functions for setting test suite timeouts.

**Exported Functions:**
- `setDefaultSuiteTimeoutcontext: Mocha.Suite` → `void`

**Exported Constants:**
- `DEFAULT_SUITE_TIMEOUT` = `120_000`

---

### apps\vscode-e2e\src\suite\tools\apply-diff.test.ts
**Purpose:** Tests the functionality of the apply_diff tool.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\execute-command.test.ts
**Purpose:** Tests the execute_command tool within the Roo Code extension.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\insert-content.test.ts
**Purpose:** Tests the insert_content tool for the Roo Code extension.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\list-files.test.ts
**Purpose:** Tests the list_files tool functionality within the extension.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\read-file.test.ts
**Purpose:** Tests the read_file tool within the Roo Code extension.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `os`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\search-and-replace.test.ts
**Purpose:** Tests the search_and_replace tool's functionality.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\search-files.test.ts
**Purpose:** Tests the search_files tool within the Roo Code extension.

**Exported Functions:**
- `suite(name: string, this: any, ...args: any[])` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\use-mcp-tool.test.ts
**Purpose:** Tests the use_mcp_tool functionality within the extension.

**Exported Functions:**
- `skip(name: string, this: any, ...args: any[])` → `any`
- `suite(name: string, this: any, ...args: any[])` → `any`
- `suiteSetup() => Promise<void>` → `any`

**Key Imports:** `assert`, `fs/promises`, `path`, `os`, `vscode`, `@roo-code/types`, `../utils`, `../test-utils`

---

### apps\vscode-e2e\src\suite\tools\write-to-file.test.ts
**Functions:** `messageHandler`, `taskStartedHandler`, `taskCompletedHandler`, `suite`, `test`

---

### apps\vscode-e2e\src\suite\utils.ts
**Purpose:** Provides utility functions for asynchronous testing, including waiting and sleeping.

**Exported Functions:**
- `waitFor(condition: (() => Promise<boolean>) | (() => boolean), { timeout, interval }?: WaitForOptions)` → `Promise<void>`
- `waitUntilAborted({ api, taskId, ...options }: WaitUntilAbortedOptions)` → `Promise<void>`
- `waitUntilCompleted({ api, taskId, ...options }: WaitUntilCompletedOptions)` → `Promise<void>`
- `sleep(ms: number)` → `Promise<void>`

**Exported Types:**
- `type WaitForOptions`: timeout, interval
- `type WaitUntilAbortedOptions`: timeout, interval, api, taskId
- `type WaitUntilCompletedOptions`: timeout, interval, api, taskId

**Key Imports:** `@roo-code/types`

---

### apps\vscode-e2e\src\types\global.d.ts
---

### apps\web-evals\next-env.d.ts
---

### apps\web-evals\next.config.ts
---

### apps\web-evals\src\actions\exercises.ts
**Purpose:** Fetches available exercises by reading directories within the evals repository.

**Exported Functions:**
- `getExercises()` → `Promise<string[]>`

**Key Imports:** `path`, `url`, `@roo-code/evals`

---

### apps\web-evals\src\actions\heartbeat.ts
**Purpose:** Retrieves the heartbeat status for a given run ID from Redis.

**Exported Functions:**
- `getHeartbeat(runId: number)` → `Promise<string | null>`

**Key Imports:** `@/lib/server/redis`

---

### apps\web-evals\src\actions\runners.ts
**Purpose:** Retrieves the list of runners associated with a given run ID from Redis.

**Exported Functions:**
- `getRunners(runId: number)` → `Promise<string[]>`

**Key Imports:** `@/lib/server/redis`

---

### apps\web-evals\src\actions\runs.ts
**Purpose:** Creates and deletes evaluation runs, managing tasks and revalidating paths.

**Exported Functions:**
- `createRun({ suite, exercises, systemPrompt, timeout, ...values }: CreateRun)` → `Promise<any>`
- `deleteRun(runId: number)` → `Promise<void>`

**Key Imports:** `path`, `fs`, `url`, `child_process`, `next/cache`, `p-map`, `@roo-code/evals`, `@/lib/schemas`

---

### apps\web-evals\src\actions\tasks.ts
**Purpose:** Retrieves tasks associated with a run ID and revalidates the path.

**Exported Functions:**
- `getTasks(runId: number)` → `Promise<any>`

**Key Imports:** `next/cache`, `@roo-code/evals`

---

### apps\web-evals\src\app\api\health\route.ts
**Purpose:** Provides a health check endpoint that returns the application status.

**Exported Functions:**
- `GET()` → `NextResponse<any>`

**Key Imports:** `next/server`

---

### apps\web-evals\src\app\api\runs\[id]\stream\route.ts
**Purpose:** Streams task events for a given run ID using Server-Sent Events (SSE).

**Exported Functions:**
- `GET(request: NextRequest, { params }: { params: Promise<{ id: string; }>; })` → `Promise<any>`
- `onMessage(data: string)` → `Promise<void>`
- `disconnect()` → `Promise<void>`

**Key Imports:** `next/server`, `@roo-code/types`, `@roo-code/evals`, `@/lib/server/sse-stream`, `@/lib/server/redis`

---

### apps\web-evals\src\app\layout.tsx
**Purpose:** Defines the root layout for the application, including theme and providers.

**Exported Functions:**
- `RootLayout({ children, }: Readonly<{ children: React.ReactNode; }>)` → `JSX.Element`

**Key Imports:** `next`, `next/font/google`, `@/components/providers`, `@/components/ui`, `@/components/layout/header`

---

### apps\web-evals\src\app\page.tsx
**Purpose:** Renders the home page, fetching and displaying evaluation runs.

**Exported Functions:**
- `Page()` → `Promise<JSX.Element>`

**Key Imports:** `@roo-code/evals`, `@/components/home/runs`

---

### apps\web-evals\src\app\runs\[id]\page.tsx
**Purpose:** Renders a specific run page, fetching run data by ID.

**Exported Functions:**
- `Page({ params }: { params: Promise<{ id: string; }>; })` → `Promise<JSX.Element>`

**Key Imports:** `@roo-code/evals`, `./run`

---

### apps\web-evals\src\app\runs\[id]\run-status.tsx
**Purpose:** Displays the status of a run, including SSE connection and heartbeat.

**Exported Functions:**
- `RunStatus({ runStatus: { sseStatus, heartbeat, runners = [] } }: { runStatus: _RunStatus; })` → `JSX.Element`

**Key Imports:** `@/hooks/use-run-status`, `@/lib/utils`

---

### apps\web-evals\src\app\runs\[id]\run.tsx
**Purpose:** Displays details for a specific run, including tasks and token usage.

**Exported Functions:**
- `Run({ run }: { run: Run; })` → `JSX.Element`

**Key Imports:** `react`, `lucide-react`, `@roo-code/evals`, `@/lib/formatters`, `@/hooks/use-run-status`, `@/components/ui`

---

### apps\web-evals\src\app\runs\[id]\task-status.tsx
**Purpose:** Displays the status of a task using icons.

**Exported Types:**
- `type TaskStatusProps`: task, running

**Key Imports:** `lucide-react`, `@roo-code/evals`

---

### apps\web-evals\src\app\runs\new\new-run.tsx
**Purpose:** Implements the form for creating a new evaluation run with settings.

**Exported Functions:**
- `NewRun()` → `JSX.Element`

**Exported Types:**
- `type CreateRun`: name, description, modelId, systemPrompt

**Key Imports:** `react`, `next/navigation`, `zod`, `@tanstack/react-query`, `react-hook-form`, `@hookform/resolvers/zod`, `fuzzysort`, `sonner`, `lucide-react`, `@roo-code/types`, `@/actions/runs`, `@/actions/exercises`, `@/lib/schemas`, `@/lib/utils`, `@/hooks/use-open-router-models`, `@/components/ui`

---

### apps\web-evals\src\app\runs\new\page.tsx
**Purpose:** Renders the new run creation page, wrapping the NewRun component.

**Exported Functions:**
- `Page()` → `JSX.Element`

**Key Imports:** `./new-run`

---

### apps\web-evals\src\app\runs\new\settings-diff.tsx
**Purpose:** Displays the difference between default and custom settings for a run.

**Exported Functions:**
- `SettingsDiff({ customSettings: { experiments: customExperiments, ...customSettings }, defaultSettings: { experiments: defaultExperiments, ...defaultSettings }, className, ...props }: SettingsDiffProps)` → `JSX.Element`
- `SettingDiff({ name, defaultValue, customValue }: { name: string; defaultValue: string; customValue: string; })` → `JSX.Element`

**Key Imports:** `react`, `@roo-code/types`, `@/lib/utils`

---

### apps\web-evals\src\components\home\run.tsx
**Purpose:** Renders a single run row with details and actions.

**Exported Functions:**
- `Run({ run, taskMetrics }: RunProps)` → `JSX.Element`

**Exported Types:**
- `type RunProps`: run, taskMetrics

**Key Imports:** `react`, `next/link`, `lucide-react`, `@roo-code/evals`, `@/actions/runs`, `@/lib/formatters`, `@/hooks/use-copy-run`, `@/components/ui`

---

### apps\web-evals\src\components\home\runs.tsx
**Purpose:** Displays a list of evaluation runs in a table.

**Exported Functions:**
- `Runs({ runs }: { runs: RunWithTaskMetrics[] })` → `JSX.Element`

**Exported Types:**
- `type RunWithTaskMetrics`: taskMetrics, id, model, passed, failed

**Key Imports:** `next/navigation`, `lucide-react`, `@roo-code/evals`, `@/components/ui`, `@/components/home/run`

---

### apps\web-evals\src\components\layout\header.tsx
**Purpose:** Renders the application header with a logo.

**Exported Functions:**
- `Header()` → `JSX.Element`

**Key Imports:** `./logo`

---

### apps\web-evals\src\components\layout\logo.tsx
**Purpose:** Renders a clickable logo component.

**Exported Functions:**
- `Logo({ width = 50, height = 32, fill = "#fff", className, ...props }: LogoProps)` → `JSX.Element`
- `HoppingLogo()` → `JSX.Element`

**Exported Types:**
- `type LogoProps`: width, height, fill, className

**Key Imports:** `react`, `next/navigation`, `react-use`, `@/lib/utils`

---

### apps\web-evals\src\components\providers\index.ts
**Purpose:** Exports all theme and query providers.

**Key Imports:** `./react-query-provider`, `./theme-provider`

---

### apps\web-evals\src\components\providers\react-query-provider.tsx
**Purpose:** Provides React Query client for data fetching.

**Exported Functions:**
- `ReactQueryProvider({ children }: { children: React.ReactNode })` → `JSX.Element`

**Key Imports:** `@tanstack/react-query`

---

### apps\web-evals\src\components\providers\theme-provider.tsx
**Purpose:** Manages application theme using next-themes.

**Exported Functions:**
- `ThemeProvider({ children, ...props }: ThemeProviderProps)` → `JSX.Element`

**Key Imports:** `react`, `next-themes`, `next/dynamic`

---

### apps\web-evals\src\components\ui\alert-dialog.tsx
**Purpose:** Provides a modal dialog component with various parts.

**Exported Functions:**
- `AlertDialog{ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Root>` → `JSX.Element`
- `AlertDialogTrigger{ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Trigger>` → `JSX.Element`
- `AlertDialogPortal{ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Portal>` → `JSX.Element`
- `AlertDialogOverlay{ className, ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Overlay>` → `JSX.Element`
- `AlertDialogContent{ className, ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Content>` → `JSX.Element`
- `AlertDialogHeader{ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Header>` → `JSX.Element`
- `AlertDialogFooter{ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Footer>` → `JSX.Element`
- `AlertDialogTitle{ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Title>` → `JSX.Element`
- `AlertDialogDescription{ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Description>` → `JSX.Element`
- `AlertDialogAction{ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Action>` → `JSX.Element`
- `AlertDialogCancel{ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Cancel>` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-alert-dialog`, `@/lib/utils`, `@/components/ui/button`

---

### apps\web-evals\src\components\ui\badge.tsx
**Purpose:** Displays status indicators or labels.

**Exported Functions:**
- `Badge{ className, variant, asChild = false, ...props }: React.ComponentProps<"span"> & VariantProps<typeof badgeVariants> & { asChild?: boolean }` → `JSX.Element`

**Key Imports:** `react`, `Slot`, `class-variance-authority`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\button.tsx
**Purpose:** Renders a clickable button with various styles and sizes.

**Exported Functions:**
- `Button{ className, variant, size, ...props }: React.ComponentProps<typeof ButtonPrimitive> & VariantProps<typeof buttonVariants>` → `React.ForwardRefExoticComponent<React.ComponentProps<typeof ButtonPrimitive> & VariantProps<typeof buttonVariants> & React.RefAttributes<HTMLButtonElement>>`

**Key Imports:** `react`, `Slot`, `class-variance-authority`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\command.tsx
**Purpose:** Provides a command palette interface for user commands.

**Exported Functions:**
- `Command{ className, ...props }: React.ComponentProps<typeof CommandPrimitive>` → `JSX.Element`
- `CommandDialog{ title = "Command Palette", description = "Search for a command to run...", children, ...props }: React.ComponentProps<typeof Dialog> & { title?: string; description?: string }` → `JSX.Element`
- `CommandInput{ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Input>` → `JSX.Element`
- `CommandList{ className, ...props }: React.ComponentProps<typeof CommandPrimitive.List>` → `JSX.Element`
- `CommandEmpty{ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Empty>` → `JSX.Element`
- `CommandGroup{ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Group>` → `JSX.Element`
- `CommandSeparator{ className, ...props }: React.ComponentProps<typeof CommandPrimitive.Separator>` → `JSX.Element`
- `CommandItem{ className, value, ...props }: React.ComponentProps<typeof CommandPrimitive.Item>` → `JSX.Element`
- `CommandShortcut{ className, ...props }: React.HTMLAttributes<HTMLSpanElement>` → `JSX.Element`

**Key Imports:** `react`, `cmdk`, `lucide-react`, `@/lib/utils`, `@/components/ui/dialog`

---

### apps\web-evals\src\components\ui\dialog.tsx
**Purpose:** Provides a modal dialog component with various parts.

**Exported Functions:**
- `Dialog{ ...props }: React.ComponentProps<typeof DialogPrimitive.Root>` → `JSX.Element`
- `DialogTrigger{ ...props }: React.ComponentProps<typeof DialogPrimitive.Trigger>` → `JSX.Element`
- `DialogPortal{ ...props }: React.ComponentProps<typeof DialogPrimitive.Portal>` → `JSX.Element`
- `DialogClose{ ...props }: React.ComponentProps<typeof DialogPrimitive.Close>` → `JSX.Element`
- `DialogOverlay{ className, ...props }: React.ComponentProps<typeof DialogPrimitive.Overlay>` → `JSX.Element`
- `DialogContent{ className, children, ...props }: React.ComponentProps<typeof DialogPrimitive.Content>` → `JSX.Element`
- `DialogHeader{ ...props }: React.ComponentProps<typeof DialogPrimitive.Header>` → `JSX.Element`
- `DialogFooter{ ...props }: React.ComponentProps<typeof DialogPrimitive.Footer>` → `JSX.Element`
- `DialogTitle{ ...props }: React.ComponentProps<typeof DialogPrimitive.Title>` → `JSX.Element`
- `DialogDescription{ ...props }: React.ComponentProps<typeof DialogPrimitive.Description>` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-dialog`, `lucide-react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\drawer.tsx
**Purpose:** Provides a drawer component for sliding panels.

**Exported Functions:**
- `Drawer{ ...props }: React.ComponentProps<typeof DrawerPrimitive.Root>` → `JSX.Element`
- `DrawerTrigger{ ...props }: React.ComponentProps<typeof DrawerPrimitive.Trigger>` → `JSX.Element`
- `DrawerPortal{ ...props }: React.ComponentProps<typeof DrawerPrimitive.Portal>` → `JSX.Element`
- `DrawerClose{ ...props }: React.ComponentProps<typeof DrawerPrimitive.Close>` → `JSX.Element`
- `DrawerOverlay{ className, ...props }: React.ComponentProps<typeof DrawerPrimitive.Overlay>` → `JSX.Element`
- `DrawerContent{ className, children, ...props }: React.ComponentProps<typeof DrawerPrimitive.Content>` → `JSX.Element`
- `DrawerHeader{ ...props }: React.ComponentProps<typeof DrawerPrimitive.Header>` → `JSX.Element`
- `DrawerFooter{ ...props }: React.ComponentProps<typeof DrawerPrimitive.Footer>` → `JSX.Element`
- `DrawerTitle{ ...props }: React.ComponentProps<typeof DrawerPrimitive.Title>` → `JSX.Element`
- `DrawerDescription{ ...props }: React.ComponentProps<typeof DrawerPrimitive.Description>` → `JSX.Element`

**Key Imports:** `react`, `vaul`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\dropdown-menu.tsx
**Purpose:** Provides a dropdown menu component.

**Exported Functions:**
- `DropdownMenu{ ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Root>` → `JSX.Element`
- `DropdownMenuPortal{ ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Portal>` → `JSX.Element`
- `DropdownMenuTrigger{ ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Trigger>` → `JSX.Element`
- `DropdownMenuContent{ className, sideOffset = 4, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Content>` → `JSX.Element`
- `DropdownMenuGroup{ ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Group>` → `JSX.Element`
- `DropdownMenuItem{ className, inset, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Item> & { inset?: boolean }` → `JSX.Element`
- `DropdownMenuCheckboxItem{ className, children, checked, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.CheckboxItem>` → `JSX.Element`
- `DropdownMenuRadioGroup{ ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.RadioGroup>` → `JSX.Element`
- `DropdownMenuRadioItem{ className, children, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.RadioItem>` → `JSX.Element`
- `DropdownMenuLabel{ className, inset, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Label> & { inset?: boolean }` → `JSX.Element`
- `DropdownMenuSeparator{ className, inset, ...props }: React.ComponentProps<typeof DropdownMenuPrimitive.Separator> & { inset?: boolean }` → `JSX.Element`
- `DropdownMenuShortcut{ className, ...props }: React.HTMLAttributes<HTMLSpanElement>` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-dropdown-menu`, `lucide-react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\form.tsx
**Purpose:** Provides form structure and validation utilities.

**Exported Functions:**
- `Form({ ...props })` → `JSX.Element`
- `FormField<TFieldValues extends FieldValues = FieldValues, TName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>>({ ...props }: ControllerProps<TFieldValues, TName>)` → `JSX.Element`
- `FormItem({ className, ...props }: React.HTMLAttributes<HTMLDivElement>)` → `JSX.Element`
- `FormLabel({ className, ...props }: React.ComponentProps<typeof LabelPrimitive.Root>)` → `JSX.Element`
- `FormControl({ ...props }: React.ComponentProps<typeof Slot>) ` → `JSX.Element`
- `FormDescription({ className, ...props }: React.HTMLAttributes<HTMLParagraphElement>)` → `JSX.Element`
- `FormMessage({ className, children, ...props }: React.ComponentProps<typeof LabelPrimitive.Root>)` → `JSX.Element`
- `useFormField()` → `{ id: string; formItemId: string; formItemName: string; formItemLabel: string; fieldState: import("@/components/ui/form").FieldState | undefined; field: import("@/components/ui/form").Field | undefined; } & import("@/components/ui/form").FormFieldContextValue`

**Key Imports:** `react`, `@radix-ui/react-label`, `Slot`, `react-hook-form`, `@/lib/utils`, `@/components/ui/label`

---

### apps\web-evals\src\components\ui\index.ts
**Purpose:** Exports all UI components for easy access.

**Key Imports:** `./alert-dialog`, `./badge`, `./button`, `./command`, `./dialog`, `./drawer`, `./dropdown-menu`, `./form`, `./input`, `./label`, `./multi-select`, `./popover`, `./scroll-area`, `./select`, `./separator`, `./slider`, `./sonner`, `./table`, `./tabs`, `./textarea`, `./tooltip`

---

### apps\web-evals\src\components\ui\input.tsx
**Purpose:** Renders a standard input field.

**Exported Functions:**
- `Input{ className, type, ...props }: React.ComponentProps<"input">` → `JSX.Element`

**Key Imports:** `react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\label.tsx
**Purpose:** Renders a label for form elements.

**Exported Functions:**
- `Label{ className, ...props }: React.ComponentProps<typeof LabelPrimitive.Root>` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-label`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\multi-select.tsx
**Purpose:** Renders a customizable multi-select component using Radix and cva.

**Exported Types:**
- `interface MultiSelectProps`: React.HTMLAttributes<HTMLDivElement>, VariantProps<typeof multiSelectVariants>, options: {, label: string, value: string

**Key Imports:** `class-variance-authority`, `fuzzysort`, `lucide-react`, `@/lib/utils`, `./badge`

---

### apps\web-evals\src\components\ui\popover.tsx
**Purpose:** Provides accessible popover components built on Radix primitives.

**Exported Functions:**
- `Popover{ ...props }: React.ComponentProps<typeof PopoverPrimitive.Root>` → `JSX.Element`
- `PopoverTrigger{ ...props }: React.ComponentProps<typeof PopoverPrimitive.Trigger>` → `JSX.Element`
- `PopoverContent{
	className,
	align = "center",
	sideOffset = 4,
	...props
}: React.ComponentProps<typeof PopoverPrimitive.Content>` → `JSX.Element`
- `PopoverAnchor{ ...props }: React.ComponentProps<typeof PopoverPrimitive.Anchor>` → `JSX.Element`

**Key Imports:** `@radix-ui/react-popover`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\scroll-area.tsx
**Purpose:** Implements a scrollable area component with custom scrollbars.

**Exported Functions:**
- `ScrollArea({ className, children, viewportRef, ...props }: ScrollAreaProps)` → `JSX.Element`
- `ScrollBar({ className, orientation = "vertical", ...props }: React.ComponentProps<typeof ScrollAreaPrimitive.ScrollAreaScrollbar>)` → `JSX.Element`

**Exported Types:**
- `type ScrollAreaProps`: React.ComponentProps<typeof ScrollAreaPrimitive.Root>, viewportRef?: React.RefObject<HTMLDivElement>

**Key Imports:** `@radix-ui/react-scroll-area`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\select.tsx
**Purpose:** Exports various components for building a custom select input interface.

**Exported Functions:**
- `Select{ ...props }: React.ComponentProps<typeof SelectPrimitive.Root>` → `JSX.Element`
- `SelectGroup{ ...props }: React.ComponentProps<typeof SelectPrimitive.Group>` → `JSX.Element`
- `SelectValue{ ...props }: React.ComponentProps<typeof SelectPrimitive.Value>` → `JSX.Element`
- `SelectTrigger({ className, size = "default", children, ...props }: React.ComponentProps<typeof SelectPrimitive.Trigger> & { size?: "sm" | "default" })` → `JSX.Element`
- `SelectContentany` → `any`
- `SelectLabelany` → `any`
- `SelectItemany` → `any`
- `SelectSeparatorany` → `any`
- `SelectScrollUpButtonany` → `any`
- `SelectScrollDownButtonany` → `any`

**Key Imports:** `@radix-ui/react-select`, `lucide-react`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\separator.tsx
**Purpose:** Renders a customizable horizontal or vertical separator line.

**Exported Functions:**
- `Separator({ className, orientation = "horizontal", decorative = true, ...props }: React.ComponentProps<typeof SeparatorPrimitive.Root>)` → `JSX.Element`

**Key Imports:** `@radix-ui/react-separator`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\slider.tsx
**Purpose:** Implements a range slider component using Radix primitives.

**Exported Functions:**
- `Slider({ className, defaultValue, value, min = 0, max = 100, ...props }: React.ComponentProps<typeof SliderPrimitive.Root>)` → `JSX.Element`

**Key Imports:** `@radix-ui/react-slider`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\sonner.tsx
**Purpose:** Renders a Sonner toast container respecting the current theme.

**Exported Functions:**
- `Toaster{ ...props }: ToasterProps` → `JSX.Element`

**Key Imports:** `next-themes`, `sonner`, `react`

---

### apps\web-evals\src\components\ui\table.tsx
**Purpose:** Exports components for structuring and styling HTML tables.

**Exported Functions:**
- `Table{ className, ...props }: React.ComponentProps<"table">` → `JSX.Element`
- `TableHeader{ className, ...props }: React.ComponentProps<"thead">` → `JSX.Element`
- `TableBody{ className, ...props }: React.ComponentProps<"tbody">` → `JSX.Element`
- `TableFooter{ className, ...props }: React.ComponentProps<"tfoot">` → `JSX.Element`
- `TableRow{ className, ...props }: React.ComponentProps<"tr">` → `JSX.Element`
- `TableHead{ className, ...props }: React.ComponentProps<"th">` → `JSX.Element`
- `TableCellany` → `any`
- `TableCaptionany` → `any`

**Key Imports:** `@/lib/utils`

---

### apps\web-evals\src\components\ui\tabs.tsx
**Purpose:** Implements tab navigation components with an animated indicator.

**Exported Functions:**
- `Tabsany` → `any`
- `TabsList({ className, ...props }, ref)` → `JSX.Element`

**Key Imports:** `@radix-ui/react-tabs`, `@/lib/utils`

---

### apps\web-evals\src\components\ui\textarea.tsx
**Purpose:** Renders a styled, resizable textarea input component.

**Exported Functions:**
- `Textarea{ className, ...props }: React.ComponentProps<"textarea">` → `JSX.Element`

**Key Imports:** `@/lib/utils`

---

### apps\web-evals\src\components\ui\tooltip.tsx
**Purpose:** Provides accessible tooltip components built on Radix primitives.

**Exported Functions:**
- `TooltipProvider{ delayDuration = 0, ...props }: React.ComponentProps<typeof TooltipPrimitive.Provider>` → `JSX.Element`
- `Tooltip{ ...props }: React.ComponentProps<typeof TooltipPrimitive.Root>` → `JSX.Element`
- `TooltipTrigger{ ...props }: React.ComponentProps<typeof TooltipPrimitive.Trigger>` → `JSX.Element`
- `TooltipContent({ className, sideOffset = 0, children, ...props }: React.ComponentProps<typeof TooltipPrimitive.Content>)` → `JSX.Element`

**Key Imports:** `@radix-ui/react-tooltip`, `@/lib/utils`

---

### apps\web-evals\src\hooks\use-copy-run.ts
**Purpose:** Manages copying a specific evaluation run to the production database.

**Exported Functions:**
- `useCopyRun(runId: number)` → `{ isPending: boolean, copyRun: (runId: number) => void, copied: boolean }`

**Key Imports:** `react`, `@tanstack/react-query`, `sonner`, `@/lib/actions`

---

### apps\web-evals\src\hooks\use-event-source.ts
**Purpose:** Hook for managing an EventSource connection with status tracking.

**Exported Functions:**
- `useEventSource({ url, withCredentials, onMessage }: UseEventSourceOptions)` → `{ sourceRef: React.MutableRefObject<EventSource | null>, status: EventSourceStatus, cleanup: () => void, createEventSource: () => void }`

**Exported Types:**
- `type EventSourceStatus`: "waiting", "connected", "error"
- `type EventSourceEvent`: Event & { data: string }
- `type UseEventSourceOptions`: url: string, withCredentials?: boolean, onMessage: (event: MessageEvent) => void

**Key Imports:** `react`

---

### apps\web-evals\src\hooks\use-open-router-models.ts
**Purpose:** Fetches and queries available models from the OpenRouter API.

**Exported Functions:**
- `getOpenRouterModels(): Promise<OpenRouterModel[]>` → `Promise<OpenRouterModel[]>`
- `useOpenRouterModels()` → `QueryObserverResult<OpenRouterModel[], Error>`

**Exported Types:**
- `type OpenRouterModel`: id: string, name: string

**Exported Constants:**
- `openRouterModelSchema` = `z.object({...})`

**Key Imports:** `zod`, `@tanstack/react-query`

---

### apps\web-evals\src\hooks\use-run-status.ts
**Purpose:** Aggregates real-time status, metrics, and usage for an evaluation run.

**Exported Functions:**
- `useRunStatus(run: Run): RunStatus` → `RunStatus`

**Exported Types:**
- `type RunStatus`: sseStatus: EventSourceStatus, heartbeat: string | null | undefined, runners: string[] | undefined, tasks: (Task & { taskMetrics: TaskMetrics | null })[] | undefined, tokenUsage: Map<number, TokenUsage & { duration?: number }>

**Key Imports:** `@tanstack/react-query`, `@roo-code/types`, `@roo-code/evals`, `@/actions/heartbeat`, `@/actions/runners`, `@/actions/tasks`, `@/hooks/use-event-source`

---

### apps\web-evals\src\lib\actions.ts
**Purpose:** Defines server actions for copying evaluation runs to production.

**Exported Functions:**
- `copyRunToProduction(runId: number)` → `Promise<{ success: boolean, message?: string, error?: string }>`

**Key Imports:** `@roo-code/evals`

---

### apps\web-evals\src\lib\formatters.ts
**Purpose:** Provides utility functions for formatting monetary, time, and token values.

**Exported Functions:**
- `formatCurrency(amount: number)` → `string`
- `formatDuration(durationMs: number)` → `string`
- `formatTokens(tokens: number)` → `string`
- `formatToolUsageSuccessRate(usage: { attempts: number; failures: number })` → `string`

**Key Imports:** `intl`

---

### apps\web-evals\src\lib\schemas.ts
**Purpose:** Defines Zod schemas and constants for creating new evaluation runs.

**Exported Types:**
- `type CreateRun`: model: string, description?: string, suite: "full" | "partial", exercises?: string[], concurrency: number, timeout: number

**Exported Constants:**
- `MODEL_DEFAULT` = `"anthropic/claude-sonnet-4"`
- `CONCURRENCY_MIN` = `1`
- `CONCURRENCY_MAX` = `25`
- `CONCURRENCY_DEFAULT` = `1`
- `TIMEOUT_MIN` = `5`
- `TIMEOUT_MAX` = `10`
- `TIMEOUT_DEFAULT` = `5`

**Key Imports:** `zod`, `@roo-code/types`

---

### apps\web-evals\src\lib\server\__tests__\sse-stream.spec.ts
---

### apps\web-evals\src\lib\server\redis.ts
**Purpose:** Manages and exports a singleton Redis client connection.

**Exported Functions:**
- `redisClient(): Promise<RedisClientType>` → `Promise<RedisClientType>`

**Key Imports:** `redis`

---

### apps\web-evals\src\lib\server\sse-stream.ts
**Functions:** `constructor`, `getResponse`

---

### apps\web-evals\src\lib\utils.ts
**Functions:** `cn`

---

### apps\web-evals\vitest.config.ts
---

### apps\web-roo-code\next.config.ts
**Functions:** `redirects`, `page`

---

### apps\web-roo-code\src\actions\evals.ts
**Functions:** `getEvalRuns`

---

### apps\web-roo-code\src\app\enterprise\page.tsx
**Functions:** `Enterprise`

---

### apps\web-roo-code\src\app\evals\evals.tsx
**Functions:** `Evals`

---

### apps\web-roo-code\src\app\evals\page.tsx
**Functions:** `Page`

---

### apps\web-roo-code\src\app\evals\plot.tsx
**Functions:** `Plot`, `renderQuadrant`, `renderCustomLabel`, `truncateText`

---

### apps\web-roo-code\src\app\evals\types.ts
---

### apps\web-roo-code\src\app\layout.tsx
**Functions:** `RootLayout`

---

### apps\web-roo-code\src\app\legal\cookies\page.tsx
**Functions:** `CookiePolicy`

---

### apps\web-roo-code\src\app\legal\subprocessors\page.tsx
**Functions:** `SubProcessors`

---

### apps\web-roo-code\src\app\page.tsx
**Functions:** `Home`

---

### apps\web-roo-code\src\app\pricing\page.tsx
**Functions:** `PricingPage`

---

### apps\web-roo-code\src\app\privacy\page.tsx
**Functions:** `Privacy`

---

### apps\web-roo-code\src\app\robots.ts
**Functions:** `robots`

---

### apps\web-roo-code\src\app\shell.tsx
**Functions:** `Shell`

---

### apps\web-roo-code\src\app\terms\page.tsx
**Functions:** `Terms`

---

### apps\web-roo-code\src\components\animated-text.tsx
**Purpose:** Renders text content with a smooth initial animation using Framer Motion.

**Exported Functions:**
- `AnimatedText({ children: React.ReactNode, className?: string })` → `JSX.Element`

**Key Imports:** `react`, `framer-motion`

---

### apps\web-roo-code\src\components\chromes\footer.tsx
**Purpose:** Displays the application footer containing links, branding, and theme information.

**Exported Functions:**
- `Footer()` → `JSX.Element`

**Key Imports:** `react`, `next/link`, `next/image`, `next-themes`, `@/lib/constants`

---

### apps\web-roo-code\src\components\chromes\index.ts
**Purpose:** Aggregates and re-exports core chrome components for easy access.

**Key Imports:** `./footer`, `./nav-bar`, `./stats-display`, `./theme-toggle`

---

### apps\web-roo-code\src\components\chromes\nav-bar.tsx
**Purpose:** Renders the main navigation bar displaying links and application statistics.

**Exported Functions:**
- `NavBar({ stars: string | null, downloads: string | null })` → `JSX.Element`

**Key Imports:** `next/link`, `next/image`, `react`, `@/lib/constants`, `@/lib/hooks/use-logo-src`

---

### apps\web-roo-code\src\components\chromes\stats-display.tsx
**Purpose:** Fetches and displays GitHub star count and VS Code download statistics.

**Exported Functions:**
- `StatsDisplay()` → `Promise<JSX.Element>`

**Key Imports:** `next/link`, `react-icons/rx`, `react-icons/vsc`, `@/lib/stats`

---

### apps\web-roo-code\src\components\chromes\theme-toggle.tsx
**Purpose:** Provides a button component allowing users to switch between light and dark themes.

**Exported Functions:**
- `ThemeToggle()` → `JSX.Element`

**Key Imports:** `react`, `next-themes`, `react-icons/rx`, `@/components/ui`

---

### apps\web-roo-code\src\components\CookieConsentWrapper.tsx
**Purpose:** Renders a GDPR-compliant cookie consent banner and manages consent event dispatching.

**Exported Functions:**
- `CookieConsentWrapper()` → `JSX.Element`

**Key Imports:** `react`, `react-cookie-consent`, `tldts`, `@roo-code/types`, `@/lib/analytics/consent-manager`

---

### apps\web-roo-code\src\components\enterprise\contact-form.tsx
**Purpose:** Provides a modal contact form for requesting demos or early access partnerships.

**Exported Functions:**
- `ContactForm({ formType: 'early-access' | 'demo', buttonText: string, buttonClassName?: string })` → `JSX.Element`

**Key Imports:** `react`, `zod`, `@/components/ui`

---

### apps\web-roo-code\src\components\homepage\animated-background.tsx
**Purpose:** Renders a dynamic canvas background featuring an animated grid and particle system.

**Exported Functions:**
- `AnimatedBackground()` → `JSX.Element`

**Key Imports:** `react`

---

### apps\web-roo-code\src\components\homepage\code-example.tsx
**Purpose:** Displays a simulated code editor interface demonstrating different AI modes via typing animation.

**Exported Functions:**
- `CodeExample()` → `JSX.Element`

**Key Imports:** `react`, `framer-motion`

---

### apps\web-roo-code\src\components\homepage\company-logos.tsx
**Purpose:** Displays a scrolling list of company logos using Framer Motion animations.

**Exported Functions:**
- `CompanyLogos()` → `JSX.Element`

**Key Imports:** `framer-motion`, `next/image`

---

### apps\web-roo-code\src\components\homepage\faq-section.tsx
**Purpose:** Renders an interactive frequently asked questions section using accordion functionality.

**Exported Functions:**
- `FAQSection()` → `JSX.Element`

**Key Imports:** `react`, `framer-motion`, `lucide-react`, `@/lib/utils`, `next/link`

---

### apps\web-roo-code\src\components\homepage\features.tsx
**Purpose:** Displays key product features using icons, titles, and descriptive text.

**Exported Functions:**
- `Features()` → `JSX.Element`

**Exported Types:**
- `interface Feature`: icon: LucideIcon, title: string, description: string, logos?: string[]

**Exported Constants:**
- `features` = `Feature[]`

**Key Imports:** `framer-motion`, `lucide-react`, `next/image`

---

### apps\web-roo-code\src\components\homepage\index.ts
**Purpose:** Aggregates and re-exports all homepage section components for modular use.

**Key Imports:** `./animated-background`, `./code-example`, `./company-logos`, `./faq-section`, `./features`

---

### apps\web-roo-code\src\components\homepage\install-section.tsx
**Purpose:** Presents a call-to-action section encouraging users to install the VS Code extension.

**Exported Functions:**
- `InstallSection({ downloads: string | null })` → `JSX.Element`

**Key Imports:** `react-icons/vsc`, `next/link`, `framer-motion`

---

### apps\web-roo-code\src\components\homepage\testimonials.tsx
**Purpose:** Displays a rotating carousel of user testimonials using Embla Carousel.

**Exported Functions:**
- `Testimonials()` → `JSX.Element`

**Exported Types:**
- `interface Testimonial`: name: string, role: string, origin: string, quote: string, stars?: number

**Exported Constants:**
- `testimonials` = `Testimonial[]`

**Key Imports:** `react`, `framer-motion`, `embla-carousel-react`, `embla-carousel-autoplay`, `lucide-react`

---

### apps\web-roo-code\src\components\homepage\whats-new-button.tsx
**Purpose:** Renders a button that triggers a modal displaying recent product updates and features.

**Exported Functions:**
- `WhatsNewButton()` → `JSX.Element`

**Key Imports:** `react`, `framer-motion`, `lucide-react`, `next/link`

---

### apps\web-roo-code\src\components\providers\google-analytics-provider.tsx
**Functions:** `GoogleAnalyticsProvider`, `if`, `gtag`, `initializeGoogleAnalytics`, `function`

---

### apps\web-roo-code\src\components\providers\index.ts
---

### apps\web-roo-code\src\components\providers\posthog-provider.tsx
**Functions:** `PageViewTracker`, `PostHogProvider`, `initializePosthog`

---

### apps\web-roo-code\src\components\providers\providers.tsx
**Functions:** `Providers`

---

### apps\web-roo-code\src\components\structured-data.tsx
**Functions:** `StructuredData`

---

### apps\web-roo-code\src\components\ui\button.tsx
---

### apps\web-roo-code\src\components\ui\chart.tsx
**Functions:** `useChart`, `getPayloadConfigFromPayload`, `ChartStyle`

---

### apps\web-roo-code\src\components\ui\index.ts
---

### apps\web-roo-code\src\components\ui\modal.tsx
**Functions:** `DialogHeader`, `DialogFooter`

---

### apps\web-roo-code\src\components\ui\scroll-button.tsx
**Functions:** `ScrollButton`, `handleClick`

---

### apps\web-roo-code\src\components\ui\table.tsx
---

### apps\web-roo-code\src\lib\analytics\consent-manager.ts
**Functions:** `hasConsent`, `dispatchConsentEvent`, `onConsentChange`, `handler`

---

### apps\web-roo-code\src\lib\constants.ts
---

### apps\web-roo-code\src\lib\format-currency.ts
**Functions:** `formatCurrency`, `parsePrice`

---

### apps\web-roo-code\src\lib\format-duration.ts
**Functions:** `formatDuration`

---

### apps\web-roo-code\src\lib\format-score.ts
**Functions:** `formatScore`

---

### apps\web-roo-code\src\lib\format-tokens.ts
**Functions:** `formatTokens`

---

### apps\web-roo-code\src\lib\hooks\index.ts
---

### apps\web-roo-code\src\lib\hooks\use-logo-src.ts
**Functions:** `useLogoSrc`

---

### apps\web-roo-code\src\lib\hooks\use-open-router-models.ts
**Functions:** `parsePrice`, `useOpenRouterModels`

---

### apps\web-roo-code\src\lib\index.ts
**Purpose:** Re-exports formatting functions for currency, duration, and scores.

---

### apps\web-roo-code\src\lib\seo.ts
**Purpose:** Defines SEO configuration including metadata and structured data.

**Exported Types:**
- `type SeoConfig`

**Exported Constants:**
- `SEO` = `object`

---

### apps\web-roo-code\src\lib\stats.ts
**Purpose:** Fetches and formats GitHub stars and VS Code extension reviews.

**Exported Functions:**
- `getGitHubStars` → `Promise<string | null>`
- `getVSCodeReviews` → `Promise<any[]>`

---

### apps\web-roo-code\src\lib\structured-data.ts
**Purpose:** Generates JSON-LD structured data for SEO optimization.

**Exported Functions:**
- `getStructuredData` → `StructuredDataGraph`

**Exported Types:**
- `interface ImageObject`: "@type", url, width, height
- `interface Organization`: "@type", "@id", name, url
- `interface WebSite`: "@type", "@id", url, name
- `interface SoftwareApplication`: "@type", "@id", name, applicationCategory
- `interface StructuredDataGraph`: "@context", "@graph"

**Key Imports:** `./seo`, `./constants`

---

### apps\web-roo-code\src\lib\utils.ts
**Purpose:** Provides utility functions, including a class name merger.

**Exported Functions:**
- `cn...inputs: ClassValue[]` → `string`

**Key Imports:** `clsx`, `tailwind-merge`

---

### apps\web-roo-code\tailwind.config.ts
**Purpose:** Configures the Tailwind CSS styles for the application.

**Key Imports:** `tailwindcss`

---

### packages\cloud\src\__mocks__\vscode.ts
---

### packages\cloud\src\__tests__\CloudService.integration.test.ts
---

### packages\cloud\src\__tests__\CloudService.test.ts
**Functions:** `expect`

---

### packages\cloud\src\__tests__\CloudSettingsService.parsing.test.ts
---

### packages\cloud\src\__tests__\CloudSettingsService.test.ts
---

### packages\cloud\src\__tests__\CloudShareService.test.ts
---

### packages\cloud\src\__tests__\RefreshTimer.test.ts
---

### packages\cloud\src\__tests__\StaticSettingsService.test.ts
---

### packages\cloud\src\__tests__\StaticTokenAuthService.spec.ts
---

### packages\cloud\src\__tests__\TelemetryClient.test.ts
---

### packages\cloud\src\__tests__\WebAuthService.spec.ts
---

### packages\cloud\src\bridge\__tests__\ExtensionChannel.test.ts
---

### packages\cloud\src\bridge\__tests__\TaskChannel.test.ts
---

### packages\cloud\src\bridge\BaseChannel.ts
**Purpose:** Defines an abstract base class for communication channels.

**Exported Functions:**
- `constructoroptions: BaseChannelOptions` → ``
- `onConnectsocket: Socket` → `Promise<void>`
- `onDisconnect` → `void`

**Exported Types:**
- `interface BaseChannelOptions`: instanceId, appProperties, gitProperties, isCloudAgent
- `class BaseChannel`: socket, instanceId, appProperties, gitProperties

**Key Imports:** `socket.io-client`, `vscode`, `@roo-code/types`

---

### packages\cloud\src\bridge\BridgeOrchestrator.ts
**Purpose:** Orchestrates communication between VSCode and the web application.

**Exported Functions:**
- `constructoroptions: BridgeOrchestratorOptions` → ``
- `connect` → `Promise<void>`
- `disconnect` → `Promise<void>`
- `handleConnectsocket: Socket` → `Promise<void>`
- `handleDisconnectreason: string` → `void`
- `handleReconnect` → `Promise<void>`

**Exported Types:**
- `interface BridgeOrchestratorOptions`: userId, socketBridgeUrl, token, provider
- `class BridgeOrchestrator`: userId, socketBridgeUrl, token, provider

**Key Imports:** `crypto`, `os`, `@roo-code/types`, `./SocketTransport.js`, `./ExtensionChannel.js`, `./TaskChannel.js`

---

### packages\cloud\src\bridge\ExtensionChannel.ts
**Purpose:** Manages the extension-level communication channel in the bridge.

**Exported Functions:**
- `constructoroptions: ExtensionChannelOptions` → ``
- `listenereventName: RooCodeEventName, listener: (...args: unknown[]) => void` → `void`

**Exported Types:**
- `interface ExtensionChannelOptions`: userId, provider
- `class ExtensionChannel`: userId, provider, extensionInstance, heartbeatInterval

**Key Imports:** `socket.io-client`, `@roo-code/types`, `./BaseChannel.js`

---

### packages\cloud\src\bridge\index.ts
**Purpose:** Exports bridge components for cloud communication.

**Key Imports:** `./BridgeOrchestrator.js`, `./SocketTransport.js`, `./BaseChannel.js`, `./ExtensionChannel.js`, `./TaskChannel.js`

---

### packages\cloud\src\bridge\SocketTransport.ts
**Purpose:** Manages the WebSocket transport layer for the bridge system.

**Exported Functions:**
- `constructoroptions: SocketTransportOptions, retryConfig?: Partial<RetryConfig>` → ``

**Exported Types:**
- `interface SocketTransportOptions`: url, socketOptions, onConnect, onDisconnect
- `class SocketTransport`: socket, connectionState, retryTimeout, isPreviouslyConnected

**Key Imports:** `socket.io-client`, `@roo-code/types`

---

### packages\cloud\src\bridge\TaskChannel.ts
**Purpose:** Manages task-level communication channels within the bridge.

**Exported Functions:**
- `constructoroptions: TaskChannelOptions` → ``
- `listenereventName: TaskBridgeEventName, listener: TaskEventListener` → `void`

**Exported Types:**
- `interface TaskChannelOptions`
- `class TaskChannel`: subscribedTasks, pendingTasks, taskListeners, eventMapping

**Key Imports:** `socket.io-client`, `@roo-code/types`, `./BaseChannel.js`

---

### packages\cloud\src\CloudAPI.ts
**Purpose:** Provides an API client for interacting with the Roo Code cloud.

**Exported Types:**
- `interface CloudAPIRequestOptions`: timeout, headers
- `class CloudAPI`: authService, log, baseUrl

**Key Imports:** `zod`, `@roo-code/types`, `./config.js`, `./utils.js`, `./errors.js`

---

### packages\cloud\src\CloudService.ts
**Purpose:** Manages the cloud service, handling authentication and settings.

**Exported Types:**
- `class CloudService`: context, authStateListener, authUserInfoListener, settingsList

**Key Imports:** `vscode`, `events`, `@roo-code/types`, `./errors.js`, `./WebAuthService.js`, `./StaticTokenAuthService.js`, `./CloudSettingsService.js`

---

### packages\cloud\src\CloudSettingsService.ts
**Purpose:** Manages and provides access to cloud-based settings.

**Exported Functions:**
- `parseExtensionSettingsResponsedata: unknown` → `object`

**Exported Types:**
- `class CloudSettingsService`

**Key Imports:** `events`, `vscode`, `zod`, `@roo-code/types`, `./config.js`, `./RefreshTimer.js`

---

### packages\cloud\src\CloudShareService.ts
**Purpose:** Provides methods to share tasks and manage sharing capabilities via the CloudAPI.

**Exported Functions:**
- `shareTasktaskId: string, visibility: ShareVisibility = "organization"` → `Promise<ShareResponse>`
- `canShareTask` → `Promise<boolean>`

**Exported Types:**
- `class CloudShareService`: cloudAPI, settingsService, log

**Key Imports:** `@roo-code/types`, `./importVscode.js`, `./CloudAPI.js`

---

### packages\cloud\src\config.ts
**Purpose:** Defines and exports configuration constants and functions for Clerk and RooCode APIs.

**Exported Functions:**
- `getClerkBaseUrl` → `string`
- `getRooCodeApiUrl` → `string`

**Exported Constants:**
- `PRODUCTION_CLERK_BASE_URL` = `https://clerk.roocode.com`
- `PRODUCTION_ROO_CODE_API_URL` = `https://app.roocode.com`

---

### packages\cloud\src\errors.ts
**Purpose:** Defines custom error classes for handling Cloud API-related errors.

**Exported Types:**
- `class CloudAPIError`: message, statusCode, responseBody
- `class TaskNotFoundError`: message, statusCode
- `class AuthenticationError`: message, statusCode
- `class NetworkError`: message
- `class InvalidClientTokenError`: message

---

### packages\cloud\src\importVscode.ts
**Purpose:** Dynamically imports the VS Code module for use in different environments.

**Exported Functions:**
- `importVscode` → `Promise<typeof import("vscode") | undefined>`

---

### packages\cloud\src\index.ts
**Purpose:** Aggregates and exports modules from different cloud-related subdirectories.

**Exported Types:**
- `type QueuedRequest`
- `type QueueStats`
- `type RetryQueueConfig`
- `type RetryQueueEvents`

**Key Imports:** `./config.js`, `./CloudService.js`, `./bridge/index.js`, `./retry-queue/index.js`

---

### packages\cloud\src\RefreshTimer.ts
**Purpose:** Provides a utility for executing a callback with configurable retry behavior.

**Exported Types:**
- `interface RefreshTimerOptions`: callback, successInterval, initialBackoffMs, maxBackoffMs

---

### packages\cloud\src\retry-queue\__tests__\RetryQueue.test.ts
---

### packages\cloud\src\retry-queue\index.ts
**Purpose:** Exports the RetryQueue class and related types for managing asynchronous operations.

**Exported Types:**
- `type QueuedRequest`
- `type QueueStats`
- `type RetryQueueConfig`
- `type RetryQueueEvents`

**Key Imports:** `./RetryQueue.js`, `./types.js`

---

### packages\cloud\src\retry-queue\RetryQueue.ts
**Purpose:** Implements a retry queue for managing and retrying failed asynchronous requests.

**Exported Types:**
- `class RetryQueue`: queue, context, config

**Key Imports:** `events`, `vscode`, `./types.js`

---

### packages\cloud\src\retry-queue\types.ts
**Purpose:** Defines the interfaces for queued requests, queue statistics, and retry queue configuration.

**Exported Types:**
- `interface QueuedRequest`: id, url, options, timestamp
- `interface QueueStats`: totalQueued, byType, oldestRequest, newestRequest
- `interface RetryQueueConfig`: maxRetries, retryDelay, maxQueueSize, persistQueue
- `interface RetryQueueEvents`

---

### packages\cloud\src\StaticSettingsService.ts
**Purpose:** Provides static settings from an environment variable, implementing the SettingsService interface.

**Exported Types:**
- `class StaticSettingsService`: settings, log

**Key Imports:** `@roo-code/types`

---

### packages\cloud\src\StaticTokenAuthService.ts
**Purpose:** Provides authentication using a static token, implementing the AuthService interface.

**Exported Types:**
- `class StaticTokenAuthService`: state, token, log

**Key Imports:** `events`, `jwt-decode`, `vscode`, `@roo-code/types`

---

### packages\cloud\src\TelemetryClient.ts
**Purpose:** Implements a base telemetry client for capturing and sending telemetry events.

**Key Imports:** `@roo-code/types`, `./config.js`, `./retry-queue/index.js`

---

### packages\cloud\src\utils.ts
**Purpose:** Provides utility functions, such as generating a user agent string.

**Exported Functions:**
- `getUserAgentcontext?: ExtensionContext` → `string`

**Key Imports:** `vscode`

---

### packages\cloud\src\WebAuthService.ts
**Purpose:** Implements web-based authentication using Clerk, managing user sessions and tokens.

**Exported Types:**
- `interface AuthService`

**Key Imports:** `crypto`, `events`, `vscode`, `zod`, `@roo-code/types`, `./config.js`, `./utils.js`, `./importVscode.js`, `./errors.js`, `./RefreshTimer.js`

---

### packages\cloud\vitest.config.ts
---

### packages\config-eslint\base.js
---

### packages\config-eslint\next.js
---

### packages\config-eslint\react.js
---

### packages\evals\drizzle.config.ts
---

### packages\evals\src\cli\index.ts
**Functions:** `main`

---

### packages\evals\src\cli\redis.ts
**Functions:** `redisClient`, `getPubSubKey`, `getRunnersKey`, `getHeartbeatKey`, `registerRunner`, `deregisterRunner`, `startHeartbeat`, `stopHeartbeat`

---

### packages\evals\src\cli\runCi.ts
**Functions:** `runCi`

---

### packages\evals\src\cli\runEvals.ts
**Functions:** `runEvals`

---

### packages\evals\src\cli\runTask.ts
**Functions:** `processTask`, `publish`, `processTaskInContainer`, `runTask`, `constructor`

---

### packages\evals\src\cli\runUnitTest.ts
**Purpose:** Executes unit tests for a specific evaluation task.

**Exported Functions:**
- `runUnitTest{ task, logger }: RunUnitTestOptions` → `Promise<void>`

**Exported Types:**
- `type RunUnitTestOptions`: task: Task, logger: Logger

**Key Imports:** `execa`, `../db/index.js`, `../exercises/index.js`, `./utils.js`, `path`

---

### packages\evals\src\cli\utils.ts
**Purpose:** Provides utility functions for logging and Git operations in evals.

**Exported Functions:**
- `getTag(caller: string, { run, task }: { run: Run; task?: Task })` → `string`
- `isDockerContainer()` → `boolean`
- `resetEvalsRepo{ run, cwd }: { run: Run; cwd: string }` → `Promise<void>`
- `commitEvalsRepoChanges{ run, cwd }: { run: Run; cwd: string }` → `Promise<void>`

**Exported Types:**
- `interface LoggerOptions`: logDir: string, filename: string, tag: string
- `class Logger`: logStream: fs.WriteStream | undefined, logFilePath: string, tag: string

**Exported Constants:**
- `UNIT_TEST_TIMEOUT` = `120000`

**Key Imports:** `../db/index.js`, `execa`, `fs`, `path`

---

### packages\evals\src\db\db.ts
**Purpose:** Manages database client connections for testing and production.

**Exported Functions:**
- `getProductionClient()` → `typeof client`
- `disconnect()` → `Promise<void>`

**Exported Types:**
- `type DatabaseOrTransaction`: typeof client | Parameters<Parameters<typeof client.transaction>[0]>[0]

**Key Imports:** `./schema.js`, `drizzle-orm/postgres-js`, `postgres`

---

### packages\evals\src\db\index.ts
**Purpose:** Exports database schema, queries, and utility functions.

**Key Imports:** `./queries/runs.js`, `./queries/tasks.js`, `./queries/taskMetrics.js`, `./queries/toolErrors.js`, `./queries/copyRun.js`, `./schema.js`, `./db.js`

---

### packages\evals\src\db\queries\__tests__\copyRun.spec.ts
---

### packages\evals\src\db\queries\__tests__\runs.test.ts
---

### packages\evals\src\db\queries\copyRun.ts
**Purpose:** Copies a database run record and its associated metrics to another database.

**Exported Functions:**
- `copyRun{ sourceDb, targetDb, runId }` → `Promise<void>`

**Key Imports:** `drizzle-orm`, `../schema.js`, `./errors.js`

---

### packages\evals\src\db\queries\errors.ts
**Purpose:** Defines custom error classes for database record operations.

**Exported Types:**
- `class RecordNotFoundError`
- `class RecordNotCreatedError`

---

### packages\evals\src\db\queries\runs.ts
**Purpose:** Handles CRUD operations and finalization for evaluation runs.

**Exported Functions:**
- `findRun(id: number)` → `Promise<Run>`
- `createRun(args: InsertRun)` → `Promise<Run>`
- `updateRun(id: number, values: UpdateRun)` → `Promise<Run>`
- `getRuns()` → `Promise<({ taskMetrics: TaskMetrics | null } & Run)[]>`
- `finishRun(runId: number)` → `Promise<void>`
- `deleteRun(id: number)` → `Promise<void>`

**Key Imports:** `./errors.js`, `../schema.js`, `../db.js`, `./taskMetrics.js`, `./tasks.js`, `drizzle-orm`

---

### packages\evals\src\db\queries\taskMetrics.ts
**Purpose:** Manages database interactions for task execution metrics.

**Exported Functions:**
- `findTaskMetrics(id: number)` → `Promise<TaskMetrics>`
- `createTaskMetrics(args: InsertTaskMetrics)` → `Promise<TaskMetrics>`
- `updateTaskMetrics(id: number, values: UpdateTaskMetrics)` → `Promise<TaskMetrics>`

**Key Imports:** `./errors.js`, `../schema.js`, `../db.js`

---

### packages\evals\src\db\queries\tasks.ts
**Purpose:** Provides database access methods for individual evaluation tasks.

**Exported Functions:**
- `findTask(id: number)` → `Promise<Task>`
- `createTask(args: InsertTask)` → `Promise<Task>`
- `updateTask(id: number, values: UpdateTask)` → `Promise<Task>`
- `getTask{ runId, language, exercise }` → `Promise<Task | undefined>`
- `getTasks(runId: number)` → `Promise<Task[]>`

**Key Imports:** `./errors.js`, `../schema.js`, `../db.js`, `../../exercises/index.js`

---

### packages\evals\src\db\queries\toolErrors.ts
**Purpose:** Inserts records for errors encountered by external tools.

**Exported Functions:**
- `createToolError(args: InsertToolError)` → `Promise<ToolError>`

**Key Imports:** `./errors.js`, `../schema.js`, `../db.js`

---

### packages\evals\src\db\schema.ts
**Purpose:** Defines the PostgreSQL database schema using Drizzle ORM.

**Exported Types:**
- `type runs`: id: integer, taskMetricsId: integer, model: text, description: text, socketPath: text, passed: integer
- `type Run`: id: number, taskMetricsId?: number | null, model: string, socketPath: string, concurrency: number
- `type InsertRun`: model: string, socketPath: string, description?: string | null, concurrency?: number, timeout?: number
- `type UpdateRun`: taskMetricsId?: number | null, model?: string, passed?: number, failed?: number
- `type tasks`: id: integer, runId: integer, taskMetricsId: integer, language: ExerciseLanguage, exercise: string

**Key Imports:** `drizzle-orm/pg-core`, `drizzle-orm`, `@roo-code/types`, `../exercises/index.js`

---

### packages\evals\src\exercises\index.ts
**Purpose:** Manages listing and retrieving available evaluation exercises.

**Exported Functions:**
- `listDirectories(basePath: string, relativePath: string)` → `Promise<string[]>`
- `getExercisesForLanguage(basePath: string, language: ExerciseLanguage)` → `Promise<string[]>`

**Exported Types:**
- `type ExerciseLanguage`

**Exported Constants:**
- `EVALS_REPO_PATH` = `path.resolve(__dirname, "..", "..", "..", "..", "..", "evals")`

**Key Imports:** `path`, `fs/promises`, `url`

---

### packages\evals\src\index.ts
**Purpose:** Aggregates and exports all public modules from the evals package.

**Key Imports:** `./db/index.js`, `./exercises/index.js`

---

### packages\evals\vitest-global-setup.ts
**Functions:** `resetTestDatabase`, `function`

---

### packages\evals\vitest.config.ts
---

### packages\ipc\src\index.ts
**Purpose:** Exports IPC client and server modules.

**Key Imports:** `./ipc-client.js`, `./ipc-server.js`

---

### packages\ipc\src\ipc-client.ts
**Purpose:** Handles client-side communication over Unix domain sockets.

**Exported Functions:**
- `sendCommand(command: TaskCommand)` → `void`
- `sendMessage(message: IpcMessage)` → `void`
- `disconnect()` → `void`

**Exported Types:**
- `class IpcClient`: _socketPath: string, _id: string, _log: (...args: unknown[]) => void, _isConnected: boolean, _clientId?: string

**Key Imports:** `node:events`, `node:crypto`, `node-ipc`, `@roo-code/types`

---

### packages\ipc\src\ipc-server.ts
**Purpose:** Manages server-side listening and broadcasting over Unix domain sockets.

**Exported Functions:**
- `listen()` → `void`
- `broadcast(message: IpcMessage)` → `void`
- `send(socket: Socket, message: IpcMessage)` → `void`

**Exported Types:**
- `class IpcServer`: _socketPath: string, _log: (...args: unknown[]) => void, _clients: Map<string, Socket>, _isListening: boolean

**Key Imports:** `node:events`, `node:net`, `node:crypto`, `node-ipc`, `@roo-code/types`

---

### packages\telemetry\src\__tests__\PostHogTelemetryClient.test.ts
---

### packages\telemetry\src\BaseTelemetryClient.ts
**Functions:** `constructor`

---

### packages\telemetry\src\index.ts
---

### packages\telemetry\src\PostHogTelemetryClient.ts
**Functions:** `constructor`

---

### packages\telemetry\src\TelemetryService.ts
**Functions:** `constructor`, `createInstance`, `instance`

---

### packages\telemetry\vitest.config.ts
---

### packages\types\src\__tests__\cloud.test.ts
---

### packages\types\src\__tests__\index.test.ts
---

### packages\types\src\__tests__\ipc.test.ts
---

### packages\types\src\__tests__\provider-settings.test.ts
---

### packages\types\src\api.ts
---

### packages\types\src\cloud.ts
---

### packages\types\src\codebase-index.ts
---

### packages\types\src\cookie-consent.ts
---

### packages\types\src\events.ts
---

### packages\types\src\experiment.ts
---

### packages\types\src\followup.ts
---

### packages\types\src\global-settings.ts
---

### packages\types\src\history.ts
---

### packages\types\src\index.ts
---

### packages\types\src\ipc.ts
---

### packages\types\src\marketplace.ts
---

### packages\types\src\mcp.ts
---

### packages\types\src\message.ts
**Purpose:** Defines the array of possible interaction types (asks) an LLM can request.

**Exported Constants:**
- `clineAsks` = `string[]`

**Key Imports:** `zod`

---

### packages\types\src\mode.ts
**Purpose:** Defines schemas and types for configuring operational modes and tool grouping.

**Exported Types:**
- `type GroupOptions`: fileRegex?: string, description?: string
- `type GroupEntry`: toolGroupsSchema | [toolGroupsSchema, GroupOptions]

**Exported Constants:**
- `groupOptionsSchema` = `z.ZodObject<...>`
- `groupEntrySchema` = `z.ZodUnion<...>`
- `modeConfigSchema` = `z.ZodObject<...>`

**Key Imports:** `zod`, `./tool.js`

---

### packages\types\src\model.ts
**Purpose:** Defines core types and constants for configuring LLM behavior and model parameters.

**Exported Functions:**
- `isModelParameter(value: string)` → `value is ModelParameter`

**Exported Types:**
- `type ReasoningEffort`: "low" | "medium" | "high"
- `type ReasoningEffortWithMinimal`: ReasoningEffort | "minimal"
- `type VerbosityLevel`: "low" | "medium" | "high"
- `type ServiceTier`: "default" | "flex" | "priority"
- `type ModelParameter`: "max_tokens" | "temperature" | "reasoning" | "include_reasoning"

**Exported Constants:**
- `reasoningEfforts` = `["low", "medium", "high"]`
- `verbosityLevels` = `["low", "medium", "high"]`
- `serviceTiers` = `["default", "flex", "priority"]`
- `modelParameters` = `["max_tokens", "temperature", "reasoning", "include_reasoning"]`
- `reasoningEffortsSchema` = `z.ZodEnum<...>`
- `reasoningEffortWithMinimalSchema` = `z.ZodUnion<...>`
- `verbosityLevelsSchema` = `z.ZodEnum<...>`
- `serviceTierSchema` = `z.ZodEnum<...>`
- `modelParametersSchema` = `z.ZodEnum<...>`
- `modelInfoSchema` = `z.ZodObject<...>`

**Key Imports:** `zod`

---

### packages\types\src\provider-settings.ts
**Purpose:** Defines constants and types for configuring dynamic and local LLM providers.

**Exported Functions:**
- `isDynamicProvider(key: string)` → `key is DynamicProvider`

**Exported Types:**
- `type DynamicProvider`: "openrouter" | "vercel-ai-gateway" | "huggingface" | ...
- `type LocalProvider`: "ollama" | "lmstudio"

**Exported Constants:**
- `DEFAULT_CONSECUTIVE_MISTAKE_LIMIT` = `3`
- `dynamicProviders` = `string[]`
- `localProviders` = `string[]`

**Key Imports:** `zod`, `./model.js`, `./codebase-index.js`, `./providers/index.js`

---

### packages\types\src\providers\__tests__\claude-code.spec.ts
---

### packages\types\src\providers\anthropic.ts
**Purpose:** Defines Anthropic model IDs, default selection, and associated metadata.

**Exported Types:**
- `type AnthropicModelId`: keyof typeof anthropicModels

**Exported Constants:**
- `anthropicDefaultModelId` = `"claude-sonnet-4-20250514"`
- `anthropicModels` = `Record<AnthropicModelId, ModelInfo>`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\bedrock.ts
**Purpose:** Defines AWS Bedrock model IDs, default selections, and associated metadata.

**Exported Types:**
- `type BedrockModelId`: keyof typeof bedrockModels

**Exported Constants:**
- `bedrockDefaultModelId` = `"anthropic.claude-sonnet-4-20250514-v1:0"`
- `bedrockDefaultPromptRouterModelId` = `"anthropic.claude-3-sonnet-20240229-v1:0"`
- `bedrockModels` = `Record<BedrockModelId, ModelInfo>`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\cerebras.ts
**Purpose:** Defines Cerebras model IDs, default selection, and associated metadata.

**Exported Types:**
- `type CerebrasModelId`: keyof typeof cerebrasModels

**Exported Constants:**
- `cerebrasDefaultModelId` = `"qwen-3-coder-480b-free"`
- `cerebrasModels` = `Record<CerebrasModelId, ModelInfo>`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\chutes.ts
**Purpose:** Defines the union type for all supported Chutes AI model identifiers.

**Exported Types:**
- `type ChutesModelId`: "deepseek-ai/DeepSeek-R1-0528", "unsloth/Llama-3.3-70B-Instruct", "Qwen/Qwen3-Coder-480B-A35B-Instruct-FP8", "zai-org/GLM-4.5-Air"

**Key Imports:** `../model.js`

---

### packages\types\src\providers\claude-code.ts
**Purpose:** Provides utilities for handling Claude model IDs and Vertex AI compatibility.

**Exported Functions:**
- `convertModelNameForVertex(modelName: string)` → `string`
- `getClaudeCodeModelId(baseModelId: ClaudeCodeModelId, useVertex?: boolean)` → `string`

**Exported Types:**
- `type ClaudeCodeModelId`: keyof typeof claudeCodeModels

**Exported Constants:**
- `claudeCodeDefaultModelId` = `"claude-sonnet-4-20250514"`
- `CLAUDE_CODE_DEFAULT_MAX_OUTPUT_TOKENS` = `16000`

**Key Imports:** `../model.js`, `./anthropic.js`

---

### packages\types\src\providers\deepinfra.ts
**Purpose:** Defines default model ID and fallback metadata for the DeepInfra provider.

**Exported Constants:**
- `deepInfraDefaultModelId` = `"Qwen/Qwen3-Coder-480B-A35B-Instruct-Turbo"`
- `deepInfraDefaultModelInfo` = `ModelInfo`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\deepseek.ts
**Purpose:** Defines DeepSeek model IDs, default selection, and associated metadata.

**Exported Types:**
- `type DeepSeekModelId`: keyof typeof deepSeekModels

**Exported Constants:**
- `deepSeekDefaultModelId` = `"deepseek-chat"`
- `deepSeekModels` = `Record<DeepSeekModelId, ModelInfo>`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\doubao.ts
**Purpose:** Defines Doubao model IDs, default selection, and associated metadata.

**Exported Constants:**
- `doubaoDefaultModelId` = `"doubao-seed-1-6-250615"`
- `doubaoModels` = `Record<string, ModelInfo>`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\featherless.ts
**Purpose:** Defines Featherless model IDs and their corresponding metadata.

**Exported Types:**
- `type FeatherlessModelId`: "deepseek-ai/DeepSeek-V3-0324", "moonshotai/Kimi-K2-Instruct", "openai/gpt-oss-120b", "Qwen/Qwen3-Coder-480B-A35B-Instruct"

**Exported Constants:**
- `featherlessModels` = `Record<FeatherlessModelId, ModelInfo>`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\fireworks.ts
**Purpose:** Defines Fireworks AI model IDs, default selection, and associated metadata.

**Exported Types:**
- `type FireworksModelId`: "accounts/fireworks/models/kimi-k2-instruct", "accounts/fireworks/models/deepseek-v3", "accounts/fireworks/models/glm-4p5", "accounts/fireworks/models/gpt-oss-120b"

**Exported Constants:**
- `fireworksDefaultModelId` = `"accounts/fireworks/models/kimi-k2-instruct-0905"`
- `fireworksModels` = `Record<FireworksModelId, ModelInfo>`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\gemini.ts
**Purpose:** Defines Google Gemini model IDs, default selection, and associated metadata.

**Exported Types:**
- `type GeminiModelId`: keyof typeof geminiModels

**Exported Constants:**
- `geminiDefaultModelId` = `"gemini-2.0-flash-001"`
- `geminiModels` = `Record<GeminiModelId, ModelInfo>`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\glama.ts
**Purpose:** Defines default model ID, metadata, and temperature setting for the Glama AI provider.

**Exported Constants:**
- `glamaDefaultModelId` = `"anthropic/claude-3-7-sonnet"`
- `glamaDefaultModelInfo` = `ModelInfo`
- `GLAMA_DEFAULT_TEMPERATURE` = `0`

**Key Imports:** `../model.js`

---

### packages\types\src\providers\groq.ts
---

### packages\types\src\providers\huggingface.ts
---

### packages\types\src\providers\index.ts
---

### packages\types\src\providers\io-intelligence.ts
---

### packages\types\src\providers\lite-llm.ts
---

### packages\types\src\providers\lm-studio.ts
---

### packages\types\src\providers\mistral.ts
---

### packages\types\src\providers\moonshot.ts
---

### packages\types\src\providers\ollama.ts
---

### packages\types\src\providers\openai.ts
---

### packages\types\src\providers\openrouter.ts
---

### packages\types\src\providers\qwen-code.ts
---

### packages\types\src\providers\requesty.ts
---

### packages\types\src\providers\roo.ts
---

### packages\types\src\providers\sambanova.ts
---

### packages\types\src\providers\unbound.ts
---

### packages\types\src\providers\vercel-ai-gateway.ts
---

### packages\types\src\providers\vertex.ts
---

### packages\types\src\providers\vscode-llm.ts
---

### packages\types\src\providers\xai.ts
**Purpose:** Defines xAI model IDs, default model, and model details.

**Exported Types:**
- `type XAIModelId`

**Exported Constants:**
- `xaiDefaultModelId` = `"grok-code-fast-1"`
- `xaiModels` = `{...}`

**Key Imports:** `type { ModelInfo } from "../model.js"`

---

### packages\types\src\providers\zai.ts
**Purpose:** Declares Z AI model IDs, default model, and model specifications.

**Exported Types:**
- `type InternationalZAiModelId`

**Exported Constants:**
- `internationalZAiDefaultModelId` = `"glm-4.5"`
- `internationalZAiModels` = `{...}`

**Key Imports:** `type { ModelInfo } from "../model.js"`, `import { ZaiApiLine } from "../provider-settings.js"`

---

### packages\types\src\single-file-read-models.ts
**Purpose:** Determines if a model should use single-file read format.

**Exported Functions:**
- `shouldUseSingleFileReadmodelId: string` → `boolean`

---

### packages\types\src\task.ts
**Purpose:** Defines the TaskProviderLike interface for task management.

**Exported Types:**
- `interface TaskProviderLike`: getCurrentTask, getRecentTasks, createTask, cancelTask, clearTask

**Key Imports:** `import { z } from "zod"`, `import type { RooCodeSettings } from "./global-settings.js"`, `import type { ClineMessage, QueuedMessage, TokenUsage } from "./message.js"`, `import type { ToolUsage, ToolName } from "./tool.js"`, `import type { StaticAppProperties, GitProperties, TelemetryProperties } from "./telemetry.js"`

---

### packages\types\src\telemetry.ts
**Purpose:** Defines telemetry settings, schema, and event names.

**Exported Types:**
- `type TelemetrySetting`
- `enum TelemetryEventName`

**Exported Constants:**
- `telemetrySettings` = `["unset", "enabled", "disabled"]`

**Key Imports:** `import { z } from "zod"`, `import { providerNames } from "./provider-settings.js"`, `import { clineMessageSchema } from "./message.js"`

---

### packages\types\src\terminal.ts
**Purpose:** Defines the CommandExecutionStatus type using Zod schema.

**Exported Types:**
- `type CommandExecutionStatus`

**Key Imports:** `import { z } from "zod"`

---

### packages\types\src\todo.ts
**Purpose:** Defines TodoStatus and TodoItem types with Zod schemas.

**Exported Types:**
- `type TodoStatus`
- `type TodoItem`

**Key Imports:** `import { z } from "zod"`

---

### packages\types\src\tool.ts
**Purpose:** Defines tool groups, names, and usage with Zod schemas.

**Exported Types:**
- `type ToolGroup`
- `type ToolName`
- `type ToolUsage`

**Exported Constants:**
- `toolGroups` = `["read", "edit", "browser", "command", "mcp", "modes"]`
- `toolNames` = `["execute_command", "read_file", "write_to_file", "apply_diff", "insert_content"]`

**Key Imports:** `import { z } from "zod"`

---

### packages\types\src\type-fu.ts
**Purpose:** Provides utility types for type manipulation and assertions.

**Exported Types:**
- `type Keys`
- `type Values`
- `type Equals`
- `type AssertEqual`

---

### packages\types\src\vscode.ts
**Purpose:** Defines VS Code related types, constants, and enums.

**Exported Types:**
- `type CodeActionId`
- `type CodeActionName`
- `type TerminalActionId`
- `type TerminalActionName`
- `type TerminalActionPromptType`
- `type CommandId`
- `type Language`

**Exported Constants:**
- `codeActionIds` = `["explainCode", "fixCode", "improveCode", "addToContext", "newTask"]`
- `terminalActionIds` = `["terminalAddToContext", "terminalFixCommand", "terminalExplainCommand"]`
- `commandIds` = `["activationCompleted", "plusButtonClicked", "promptsButtonClicked", "mcpButtonClicked", "historyButtonClicked"]`
- `languages` = `["ca", "de", "en", "es", "fr", "hi", "id", "it", "ja"]`

**Key Imports:** `import { z } from "zod"`

---

### packages\types\tsup.config.ts
---

### packages\types\vitest.config.ts
---

### scripts\find-missing-i18n-key.js
**Purpose:** Finds missing i18n keys in component files across locales.

**Key Imports:** `const fs = require("fs")`, `const path = require("path")`

---

### scripts\find-missing-translations.js
**Purpose:** Identifies missing translations in locale files based on arguments.

**Key Imports:** `const path = require("path")`, `const { promises: fs } = require("fs")`

---

### scripts\install-vsix.js
**Purpose:** Installs a VSIX package for the Roo Code extension.

**Key Imports:** `const { execSync } = require("child_process")`, `const fs = require("fs")`, `const readline = require("readline")`

---

### scripts\update-contributors.js
**Purpose:** This script fetches GitHub contributors and updates the README files.

**Exported Functions:**
- `parseLinkHeaderheader: string` → `object`
- `httpGeturl: string, options: object` → `Promise<string>`
- `fetchContributorsPageurl: string` → `Promise<any[]>`
- `fetchContributorsinitialUrl: string` → `Promise<any[]>`
- `readReadmereadmePath: string` → `Promise<string>`
- `formatContributorsSectioncontributors: any[]` → `string`
- `updateReadmereadmeContent: string, contributorsSection: string` → `string`
- `writeReadmereadmePath: string, readmeContent: string` → `Promise<void>`
- `findLocalizedReadmeslocalesDir: string` → `Promise<string[]>`
- `updateLocalizedReadmereadmePath: string, contributorsSection: string` → `Promise<void>`
- `main` → `Promise<void>`
- `createCellcontributor: any` → `string`

**Key Imports:** `https`, `fs`, `util`, `path`

---

### src\__mocks__\fs\promises.ts
**Purpose:** Mocks the Node.js fs/promises API for file system operations in tests.

**Exported Functions:**
- `ensureDirectoryExists(path: string)` → `void`

**Key Imports:** `vitest`

---

### src\__mocks__\vscode.js
**Purpose:** Provides mock implementations for the VS Code API objects.

**Exported Functions:**
- `mockEventEmitter()` → `{ event: () => () => {}, fire: () => {}, dispose: () => {} }`
- `constructor()` → `mockRange`

**Exported Types:**
- `class mockSelection`: start, end, anchor, active

---

### src\__tests__\command-integration.spec.ts
**Purpose:** Integrates and tests command discovery and loading functionality.

**Exported Functions:**
- `describe(name: string, fn: () => void)` → `void`
- `it(name: string, fn: () => Promise<void>)` → `void`

**Key Imports:** `path`, `../services/command/commands`

---

### src\__tests__\command-mentions.spec.ts
**Purpose:** Tests parsing text for command mentions using mocked dependencies.

**Exported Functions:**
- `callParseMentions(text: string)` → `Promise<any>`
- `describe(name: string, fn: () => void)` → `void`

**Key Imports:** `../core/mentions`, `../services/browser/UrlContentFetcher`, `../services/command/commands`

---

### src\__tests__\commands.spec.ts
**Purpose:** Tests utility functions for command file name and markdown identification.

**Exported Functions:**
- `describe(name: string, fn: () => void)` → `void`
- `getCommandNameFromFile(fileName: string)` → `string`
- `isMarkdownFile(fileName: string)` → `boolean`

**Key Imports:** `../services/command/commands`

---

### src\__tests__\dist_assets.spec.ts
**Purpose:** Verifies the presence of necessary bundled assets in the distribution folder.

**Exported Functions:**
- `describe(name: string, fn: () => void)` → `void`
- `it(name: string, fn: () => void)` → `void`

**Key Imports:** `fs`, `path`

---

### src\__tests__\extension.spec.ts
**Purpose:** Mocks VSCode API and CloudService for extension activation testing.

**Exported Functions:**
- `instance()` → `any`

**Key Imports:** `vscode`, `@roo-code/types`, `@dotenvx/dotenvx`, `@roo-code/cloud`

---

### src\__tests__\migrateSettings.spec.ts
**Purpose:** Tests the logic for migrating legacy extension settings to new formats.

**Exported Functions:**
- `describe(name: string, fn: () => void)` → `void`

**Key Imports:** `vscode`, `path`, `fs/promises`, `../utils/fs`, `../shared/globalFileNames`, `../utils/migrateSettings`

---

### src\activate\__tests__\CodeActionProvider.spec.ts
---

### src\activate\__tests__\registerCommands.spec.ts
---

### src\activate\CodeActionProvider.ts
**Purpose:** This file provides code actions for the VS Code extension.

**Exported Types:**
- `class CodeActionProvider`

**Exported Constants:**
- `TITLES` = `{"EXPLAIN":"Explain with Roo Code","FIX":"Fix with Roo Code","IMPROVE":"Improve with Roo Code","ADD_TO_CONTEXT":"Add to Roo Code","NEW_TASK":"New Roo Code Task"}`

**Key Imports:** `vscode`, `@roo-code/types`, `../shared/package`, `../utils/commands`, `../integrations/editor/EditorUtils`

---

### src\activate\handleTask.ts
**Purpose:** This file handles the creation of new tasks.

**Exported Functions:**
- `handleNewTaskparams: { prompt?: string } | null | undefined` → `Promise<void>`

**Key Imports:** `vscode`, `../shared/package`, `../core/webview/ClineProvider`, `../i18n`

---

### src\activate\handleUri.ts
**Purpose:** This file handles URI requests for authentication callbacks.

**Exported Functions:**
- `handleUriuri: vscode.Uri` → `Promise<void>`

**Key Imports:** `vscode`, `@roo-code/cloud`, `../core/webview/ClineProvider`

---

### src\activate\humanRelay.ts
**Purpose:** This file manages callbacks for human relay responses.

**Exported Functions:**
- `registerHumanRelayCallbackrequestId: string, callback: (response: string | undefined) => void` → `void`
- `unregisterHumanRelayCallbackrequestId: string` → `void`
- `handleHumanRelayResponseresponse: { requestId: string; text?: string; cancelled?: boolean }` → `void`

---

### src\activate\index.ts
**Purpose:** This file exports functions for activating the extension.

**Exported Types:**
- `type handleUri`
- `type registerCommands`
- `type registerCodeActions`
- `type registerTerminalActions`
- `type CodeActionProvider`

**Key Imports:** `./handleUri`, `./registerCommands`, `./registerCodeActions`, `./registerTerminalActions`, `./CodeActionProvider`

---

### src\activate\registerCodeActions.ts
**Purpose:** This file registers code actions for the extension.

**Exported Functions:**
- `registerCodeActionscontext: vscode.ExtensionContext` → `void`

**Key Imports:** `vscode`, `@roo-code/types`, `../utils/commands`, `../integrations/editor/EditorUtils`, `../core/webview/ClineProvider`

---

### src\activate\registerCommands.ts
**Purpose:** This file registers commands for the VS Code extension.

**Exported Functions:**
- `getVisibleProviderOrLogoutputChannel: vscode.OutputChannel` → `ClineProvider | undefined`
- `getPanel` → `vscode.WebviewPanel | vscode.WebviewView | undefined`
- `setPanelpanel: vscode.WebviewPanel | vscode.WebviewView | undefined` → `void`
- `registerCommandscontext: vscode.ExtensionContext` → `void`
- `openClineInNewTab` → `Promise<void>`

**Key Imports:** `vscode`, `delay`, `@roo-code/types`, `@roo-code/telemetry`, `../shared/package`

---

### src\activate\registerTerminalActions.ts
**Purpose:** This file registers terminal actions for the extension.

**Exported Functions:**
- `registerTerminalActionscontext: vscode.ExtensionContext` → `void`

**Key Imports:** `vscode`, `@roo-code/types`, `../utils/commands`, `../core/webview/ClineProvider`, `../integrations/terminal/Terminal`

---

### src\api\index.ts
**Purpose:** This file builds API handlers for different providers.

**Exported Functions:**
- `buildApiHandlerproviderSettings: ProviderSettings` → `ApiHandler`

**Exported Types:**
- `interface SingleCompletionHandler`: completePrompt
- `interface ApiHandlerCreateMessageMetadata`: mode, taskId, previousResponseId, suppressPreviousResponseId, responseShouldBeStored

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `./transform/stream`, `./providers/GlamaHandler`, `./providers/AnthropicHandler`

---

### src\api\providers\__tests__\anthropic-vertex.spec.ts
**Functions:** `await`

---

### src\api\providers\__tests__\anthropic.spec.ts
**Functions:** `await`

---

### src\api\providers\__tests__\bedrock-custom-arn.spec.ts
**Functions:** `describe`, `createHandler`, `mockImplementation`, `fn`, `constructor`

---

### src\api\providers\__tests__\bedrock-error-handling.spec.ts
**Functions:** `next`, `await`

---

### src\api\providers\__tests__\bedrock-inference-profiles.spec.ts
**Functions:** `createHandler`

---

### src\api\providers\__tests__\bedrock-invokedModelId.spec.ts
**Functions:** `createMockStream`, `await`

---

### src\api\providers\__tests__\bedrock-reasoning.spec.ts
**Functions:** `mockResolvedValue`, `await`

---

### src\api\providers\__tests__\bedrock-vpc-endpoint.spec.ts
---

### src\api\providers\__tests__\bedrock.spec.ts
---

### src\api\providers\__tests__\cerebras.spec.ts
---

### src\api\providers\__tests__\chutes.spec.ts
**Functions:** `await`, `next`

---

### src\api\providers\__tests__\claude-code-caching.spec.ts
**Functions:** `await`

---

### src\api\providers\__tests__\claude-code.spec.ts
**Functions:** `await`

---

### src\api\providers\__tests__\constants.spec.ts
---

### src\api\providers\__tests__\deepseek.spec.ts
**Functions:** `await`, `testProcessUsageMetrics`

---

### src\api\providers\__tests__\featherless.spec.ts
**Functions:** `await`

---

### src\api\providers\__tests__\fireworks.spec.ts
**Functions:** `next`, `await`

---

### src\api\providers\__tests__\gemini-handler.spec.ts
**Functions:** `mockReturnValue`

---

### src\api\providers\__tests__\gemini.spec.ts
**Purpose:** Tests GeminiHandler's constructor and message creation functionality thoroughly.

**Exported Functions:**
- `createMessagemockMessages: Anthropic.Messages.MessageParam[], systemPrompt: string` → `Promise<any>`

**Exported Types:**
- `class GeminiHandler`: options: any, createMessage: function, completePrompt: function

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `i18next`, `../gemini`

---

### src\api\providers\__tests__\glama.spec.ts
**Purpose:** Tests GlamaHandler's interaction with OpenAI and model fetching.

**Key Imports:** `@anthropic-ai/sdk`, `../glama`, `../../../shared/api`, `openai`

---

### src\api\providers\__tests__\groq.spec.ts
**Purpose:** Tests GroqHandler's API key usage and model selection.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`, `../groq`

---

### src\api\providers\__tests__\io-intelligence.spec.ts
**Purpose:** Tests IOIntelligenceHandler's OpenAI integration and model fetching.

**Key Imports:** `@anthropic-ai/sdk`, `../io-intelligence`, `../../../shared/api`

---

### src\api\providers\__tests__\lite-llm.spec.ts
**Purpose:** Tests LiteLLMHandler's model handling and OpenAI interaction.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `../lite-llm`, `../../../shared/api`, `@roo-code/types`

---

### src\api\providers\__tests__\lm-studio-timeout.spec.ts
**Purpose:** Tests LmStudioHandler's timeout configuration with OpenAI.

**Key Imports:** `../lm-studio`, `../../../shared/api`, `../utils/timeout-config`, `openai`

---

### src\api\providers\__tests__\lmstudio.spec.ts
**Purpose:** Tests LmStudioHandler's message handling and OpenAI interaction.

**Key Imports:** `../lm-studio`, `../../../shared/api`, `@anthropic-ai/sdk`, `openai`

---

### src\api\providers\__tests__\mistral.spec.ts
**Purpose:** Tests MistralHandler's streaming and completion with Mistral API.

**Key Imports:** `@anthropic-ai/sdk`, `../mistral`, `../../../shared/api`, `../../transform/stream`, `@mistralai/mistralai`

---

### src\api\providers\__tests__\moonshot.spec.ts
**Purpose:** Tests MoonshotHandler's token usage and OpenAI interaction.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`

---

### src\api\providers\__tests__\native-ollama.spec.ts
**Purpose:** Tests NativeOllamaHandler's message streaming from Ollama.

**Key Imports:** `../native-ollama`, `../../../shared/api`, `ollama`

---

### src\api\providers\__tests__\ollama-timeout.spec.ts
**Purpose:** Tests OllamaHandler's timeout configuration with OpenAI.

**Key Imports:** `../ollama`, `../../../shared/api`, `../utils/timeout-config`, `openai`

---

### src\api\providers\__tests__\ollama.spec.ts
**Purpose:** Tests OllamaHandler's message handling and OpenAI interaction.

**Key Imports:** `@anthropic-ai/sdk`, `../ollama`, `../../../shared/api`, `openai`

---

### src\api\providers\__tests__\openai-native-usage.spec.ts
**Purpose:** Tests OpenAiNativeHandler's usage normalization for token details.

**Key Imports:** `vitest`, `../openai-native`, `@roo-code/types`

---

### src\api\providers\__tests__\openai-native.spec.ts
**Purpose:** Tests OpenAiNativeHandler's constructor and message creation.

**Key Imports:** `@anthropic-ai/sdk`, `../openai-native`, `../../../shared/api`, `openai`

---

### src\api\providers\__tests__\openai-timeout.spec.ts
**Purpose:** This file tests OpenAI handler timeout configurations with mocked dependencies.

**Key Imports:** `../openai`, `../../../shared/api`, `../utils/timeout-config`, `openai`

---

### src\api\providers\__tests__\openai-usage-tracking.spec.ts
**Purpose:** This file tests OpenAI handler usage tracking for streaming and non-streaming responses.

**Key Imports:** `@anthropic-ai/sdk`, `../../../shared/api`, `../openai`, `openai`

---

### src\api\providers\__tests__\openai.spec.ts
**Purpose:** This file tests the OpenAI handler and model retrieval functionality.

**Exported Functions:**
- `getOpenAiModels()` → `Promise<OpenAI.Models.Model[]>`

**Key Imports:** `../openai`, `../../../shared/api`, `@anthropic-ai/sdk`, `openai`, `@roo-code/types`

---

### src\api\providers\__tests__\openrouter.spec.ts
**Purpose:** This file tests the OpenRouter handler with mocked dependencies.

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `../openrouter`, `../../../shared/api`, `../../../shared/package`

---

### src\api\providers\__tests__\requesty.spec.ts
**Purpose:** This file tests the Requesty handler with mocked dependencies.

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `../requesty`, `../../../shared/api`, `../../../shared/package`

---

### src\api\providers\__tests__\roo.spec.ts
**Purpose:** This file tests the Roo handler with mocked OpenAI client and CloudService.

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `../../../shared/api`, `openai`

---

### src\api\providers\__tests__\sambanova.spec.ts
**Purpose:** This file tests the SambaNova handler with mocked OpenAI client.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`, `../sambanova`

---

### src\api\providers\__tests__\unbound.spec.ts
**Purpose:** This file tests the Unbound handler with mocked dependencies.

**Key Imports:** `@anthropic-ai/sdk`, `../../../shared/api`, `../unbound`

---

### src\api\providers\__tests__\vercel-ai-gateway.spec.ts
**Purpose:** This file tests the Vercel AI Gateway handler with mocked dependencies.

**Exported Constants:**
- `VERCEL_AI_GATEWAY_DEFAULT_TEMPERATURE` = `0.7`

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `../vercel-ai-gateway`, `../../../shared/api`, `@roo-code/types`

---

### src\api\providers\__tests__\vertex.spec.ts
**Purpose:** This file tests the Vertex handler's message creation and streaming responses.

**Key Imports:** `@anthropic-ai/sdk`, `../../transform/stream`, `i18next`, `../vertex`

---

### src\api\providers\__tests__\vscode-lm.spec.ts
**Purpose:** This file tests the VsCodeLm handler with mocked VS Code API.

**Key Imports:** `vscode`, `../vscode-lm`, `../../../shared/api`

---

### src\api\providers\__tests__\xai.spec.ts
**Purpose:** This file tests the XAI handler with mocked OpenAI client.

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`, `../xai`

---

### src\api\providers\__tests__\zai.spec.ts
**Purpose:** This file tests the ZAi handler with mocked OpenAI client.

**Exported Constants:**
- `ZAI_DEFAULT_TEMPERATURE` = `0.7`

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`, `../zai`

---

### src\api\providers\anthropic-vertex.ts
**Purpose:** This file provides an API handler for Anthropic on Vertex AI.

**Exported Types:**
- `class AnthropicVertexHandler`

**Key Imports:** `google-auth-library`, `@anthropic-ai/sdk`, `@anthropic-ai/vertex-sdk`, `@roo-code/types`, `../../shared/api`

---

### src\api\providers\anthropic.ts
**Purpose:** This file provides an API handler for Anthropic models.

**Exported Types:**
- `class AnthropicHandler`

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `../../shared/api`, `../transform/stream`, `../transform/model-params`

---

### src\api\providers\base-openai-compatible-provider.ts
**Purpose:** This file provides a base class for OpenAI compatible providers.

**Exported Types:**
- `class BaseOpenAiCompatibleProvider`

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/stream`

---

### src\api\providers\base-provider.ts
**Purpose:** This file defines a base class for API providers.

**Exported Types:**
- `class BaseProvider`

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `../transform/stream`, `../../utils/countTokens`

---

### src\api\providers\bedrock.ts
**Purpose:** This file provides an API handler for AWS Bedrock models.

**Key Imports:** `@aws-sdk/client-bedrock-runtime`, `@aws-sdk/credential-providers`, `@anthropic-ai/sdk`, `@roo-code/types`, `../transform/stream`

---

### src\api\providers\cerebras.ts
**Purpose:** Provides an interface for interacting with the Cerebras API.

**Exported Functions:**
- `stripThinkingTokens(text: string): string` → `string`
- `flattenMessageContent(content: any): string` → `string`

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `../../shared/api`, `../transform/stream`, `../transform/openai-format`

---

### src\api\providers\chutes.ts
**Purpose:** Handles communication with the Chutes API, compatible with OpenAI.

**Key Imports:** `@roo-code/types`, `@anthropic-ai/sdk`, `openai`, `../../shared/api`, `../transform/r1-format`

---

### src\api\providers\claude-code.ts
**Purpose:** Provides an interface for the Claude Code API.

**Exported Types:**
- `class ClaudeCodeHandler`: options

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `..`, `../transform/stream`, `../../integrations/claude-code/run`

---

### src\api\providers\constants.ts
**Purpose:** Defines default headers for API requests.

**Exported Constants:**
- `DEFAULT_HEADERS` = `{
	"HTTP-Referer": "https://github.com/RooVetGit/Roo-Cline",
	"X-Title": "Roo Code",
	"User-Agent": `RooCode/${Package.version}`,
}`

**Key Imports:** `../../shared/package`

---

### src\api\providers\deepinfra.ts
**Purpose:** Handles communication with the DeepInfra API.

**Exported Types:**
- `class DeepInfraHandler`

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/stream`

---

### src\api\providers\deepseek.ts
**Purpose:** Handles communication with the DeepSeek API, compatible with OpenAI.

**Exported Types:**
- `class DeepSeekHandler`

**Key Imports:** `@roo-code/types`, `../../shared/api`, `../transform/stream`, `../transform/model-params`, `./openai`

---

### src\api\providers\doubao.ts
**Purpose:** Handles communication with the Doubao API, compatible with OpenAI.

**Exported Types:**
- `class DoubaoHandler`

**Key Imports:** `./openai`, `../../shared/api`, `@roo-code/types`, `../transform/model-params`, `../transform/stream`

---

### src\api\providers\fake-ai.ts
**Purpose:** Provides a fake AI implementation for testing and development.

**Exported Types:**
- `interface FakeAI`: id, removeFromCache, createMessage, getModel, countTokens, completePrompt
- `class FakeAIHandle`

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `../index`, `../../shared/api`, `../transform/stream`

---

### src\api\providers\featherless.ts
**Purpose:** Handles communication with the Featherless API, compatible with OpenAI.

**Exported Types:**
- `class FeatherlessHandler`

**Key Imports:** `@roo-code/types`, `@anthropic-ai/sdk`, `openai`, `../../shared/api`, `../transform/r1-format`

---

### src\api\providers\fetchers\__tests__\litellm.spec.ts
---

### src\api\providers\fetchers\__tests__\lmstudio.test.ts
---

### src\api\providers\fetchers\__tests__\modelCache.spec.ts
---

### src\api\providers\fetchers\__tests__\ollama.test.ts
---

### src\api\providers\fetchers\__tests__\openrouter.spec.ts
---

### src\api\providers\fetchers\__tests__\vercel-ai-gateway.spec.ts
---

### src\api\providers\fetchers\deepinfra.ts
**Purpose:** Fetches model information from the DeepInfra API.

**Exported Functions:**
- `getDeepInfraModels(apiKey?: string, baseUrl?: string): Promise<Record<string, ModelInfo>>` → `Promise<Record<string, ModelInfo>>`

**Key Imports:** `axios`, `zod`, `@roo-code/types`, `../constants`

---

### src\api\providers\fetchers\glama.ts
**Purpose:** Fetches model information from the Glama API.

**Exported Functions:**
- `getGlamaModels(): Promise<Record<string, ModelInfo>>` → `Promise<Record<string, ModelInfo>>`

**Key Imports:** `axios`, `@roo-code/types`, `../../../shared/cost`

---

### src\api\providers\fetchers\huggingface.ts
**Purpose:** Fetches and caches model information from Hugging Face.

**Exported Functions:**
- `parseHuggingFaceModel(rawModel: any): ModelInfo` → `ModelInfo`
- `getHuggingFaceModels(apiKey?: string): Promise<Record<string, ModelInfo>>` → `Promise<Record<string, ModelInfo>>`
- `getCachedHuggingFaceModels(apiKey?: string): Promise<Record<string, ModelInfo>>` → `Promise<Record<string, ModelInfo>>`
- `getCachedRawHuggingFaceModels(): Promise<any[]>` → `Promise<any[]>`
- `clearHuggingFaceCache(): void` → `void`
- `getHuggingFaceModelsWithMetadata(apiKey?: string): Promise<Record<string, ModelInfo>>` → `Promise<Record<string, ModelInfo>>`

**Exported Types:**
- `type HuggingFaceProvider`: provider, status, supports_tools, supports_structured_output, context_length, pricing

**Key Imports:** `axios`, `zod`, `@roo-code/types`, `../../../shared/api`

---

### src\api\providers\fetchers\io-intelligence.ts
**Purpose:** Fetches and caches model information from IO Intelligence.

**Exported Functions:**
- `parseIOIntelligenceModel(rawModel: any): ModelInfo` → `ModelInfo`
- `getIOIntelligenceModels(apiKey?: string): Promise<Record<string, ModelInfo>>` → `Promise<Record<string, ModelInfo>>`
- `getCachedIOIntelligenceModels(apiKey?: string): Promise<Record<string, ModelInfo>>` → `Promise<Record<string, ModelInfo>>`
- `clearIOIntelligenceCache(): void` → `void`

**Exported Types:**
- `type IOIntelligenceModel`: id, object, created, owned_by, max_model_len

**Key Imports:** `axios`, `zod`, `@roo-code/types`, `../../../shared/api`

---

### src\api\providers\fetchers\litellm.ts
**Purpose:** Fetches model information from a LiteLLM server.

**Exported Functions:**
- `getLiteLLMModels(apiKey: string, baseUrl: string): Promise<ModelRecord>` → `Promise<ModelRecord>`

**Key Imports:** `axios`, `@roo-code/types`, `../../../shared/api`, `../constants`

---

### src\api\providers\fetchers\lmstudio.ts
**Purpose:** Fetches and parses model information from LM Studio.

**Exported Functions:**
- `hasLoadedFullDetails(modelId: string): boolean` → `boolean`
- `forceFullModelDetailsLoad(baseUrl: string, modelId: string): Promise<void>` → `Promise<void>`
- `parseLMStudioModel(rawModel: LLMInstanceInfo | LLMInfo): ModelInfo` → `ModelInfo`

**Key Imports:** `axios`, `@lmstudio/sdk`, `@roo-code/types`, `./modelCache`

---

### src\api\providers\fetchers\modelCache.ts
**Purpose:** Caches and retrieves model records for various providers.

**Exported Functions:**
- `writeModels(router: RouterName, data: ModelRecord)` → `Promise<void>`
- `readModels(router: RouterName)` → `Promise<ModelRecord | undefined>`

**Key Imports:** `node-cache`, `@roo-code/types`, `../../../utils/safeWriteJson`, `../../../core/config/ContextProxy`, `../../../utils/storage`

---

### src\api\providers\fetchers\modelEndpointCache.ts
**Purpose:** Caches and retrieves model endpoint configurations persistently.

**Exported Functions:**
- `getCacheKey(router: RouterName, modelId: string)` → `string`
- `writeModelEndpoints(key: string, data: ModelRecord)` → `Promise<void>`
- `readModelEndpoints(key: string)` → `Promise<ModelRecord | undefined>`
- `getModelEndpoints({ router, modelId, endpoint }: { router: RouterName, modelId?: string, endpoint?: st })` → `Promise<ModelInfo>`

**Key Imports:** `node-cache`, `../../../utils/safeWriteJson`, `../../../core/config/ContextProxy`, `../../../utils/storage`, `../../../shared/api`

---

### src\api\providers\fetchers\ollama.ts
**Purpose:** Fetches and parses model information from a local Ollama instance.

**Exported Functions:**
- `parseOllamaModel(rawModel: OllamaModelInfoResponse)` → `ModelInfo`

**Key Imports:** `axios`, `@roo-code/types`, `zod`

---

### src\api\providers\fetchers\openrouter.ts
**Purpose:** Defines schemas and fetches model data from the OpenRouter API.

**Exported Types:**
- `type OpenRouterBaseModel`: name, description, context_length, max_completion_tokens, pricing
- `type openRouterModelSchema`: id, architecture, top_provider, supported_parameters
- `type OpenRouterModel`: id, architecture, top_provider, supported_parameters

**Key Imports:** `axios`, `@roo-code/types`, `zod`, `../../../shared/api`, `../../../shared/cost`

---

### src\api\providers\fetchers\requesty.ts
**Purpose:** Fetches and parses available models from a Requesty service instance.

**Exported Functions:**
- `getRequestyModels(baseUrl?: string, apiKey?: string)` → `Promise<Record<string, ModelInfo>>`

**Key Imports:** `axios`, `@roo-code/types`, `../../../shared/cost`, `../../../shared/utils/requesty`

---

### src\api\providers\fetchers\unbound.ts
**Purpose:** Fetches and maps model information from the Unbound API.

**Exported Functions:**
- `getUnboundModels(apiKey?: string | null)` → `Promise<Record<string, ModelInfo>>`

**Key Imports:** `axios`, `@roo-code/types`

---

### src\api\providers\fetchers\vercel-ai-gateway.ts
**Purpose:** Fetches and parses model data from the Vercel AI Gateway.

**Exported Types:**
- `type VercelAiGatewayModel`: id, name, context_window, max_tokens, pricing

**Key Imports:** `axios`, `zod`, `@roo-code/types`, `../../../shared/api`, `../../../shared/cost`

---

### src\api\providers\fireworks.ts
**Purpose:** Handles API interactions for the Fireworks provider.

**Exported Types:**
- `class FireworksHandler`: providerName, baseURL, apiKey, defaultProviderModelId, providerModels

**Key Imports:** `@roo-code/types`, `../../shared/api`, `./base-openai-compatible-provider`

---

### src\api\providers\gemini.ts
**Purpose:** Manages API calls and cost calculation for Google Gemini/Vertex AI.

**Exported Types:**
- `class GeminiHandler`: options, client, getModel, calculateCost

**Key Imports:** `@google/genai`, `@roo-code/types`, `../../shared/api`, `../../shared/safeJsonParse`, `../transform/gemini-format`, `../transform/stream`, `../transform/model-params`, `../index`, `./base-provider`

---

### src\api\providers\glama.ts
**Purpose:** Provides a handler for Glama AI API requests, extending RouterProvider for message creation.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`

**Exported Types:**
- `class GlamaHandler`: constructor(options: ApiHandlerOptions), createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream

**Exported Constants:**
- `DEFAULT_HEADERS` = `{"X-Glama-Metadata": JSON.stringify({ labels: [{ key: "app", value: "vscode.publisher.name" }] })}`

**Key Imports:** `@anthropic-ai/sdk`, `axios`, `openai`, `@roo-code/types`, `../../shared/package`

---

### src\api\providers\groq.ts
**Purpose:** Implements a handler for Groq API, extending an OpenAI-compatible provider.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`

**Exported Types:**
- `interface GroqUsage`: prompt_tokens_details?: { cached_tokens?: number }
- `class GroqHandler`: constructor(options: ApiHandlerOptions), createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream

**Key Imports:** `@roo-code/types`, `@anthropic-ai/sdk`, `openai`, `../../shared/api`, `../transform/stream`

---

### src\api\providers\huggingface.ts
**Purpose:** Manages API requests for Hugging Face models, including model caching.

**Exported Types:**
- `class HuggingFaceHandler`: constructor(options: ApiHandlerOptions), private client: OpenAI, private options: ApiHandlerOptions, private modelCache: ModelRecord | null

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `../../shared/api`, `../transform/stream`, `../index`

---

### src\api\providers\human-relay.ts
**Purpose:** Provides a human-assisted message processing flow for API interactions.

**Exported Functions:**
- `countTokens(_content: Array<Anthropic.Messages.ContentBlockParam>): Promise<number>` → `Promise<number>`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`

**Exported Types:**
- `class HumanRelayHandler`: countTokens(_content: Array<Anthropic.Messages.ContentBlockParam>): Promise<number>, createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream

**Key Imports:** `@anthropic-ai/sdk`, `vscode`, `@roo-code/types`, `../../utils/commands`, `../transform/stream`

---

### src\api\providers\index.ts
**Purpose:** Exports various AI provider handlers for unified access.

**Exported Constants:**
- `AnthropicVertexHandler` = `from ./anthropic-vertex`
- `AnthropicHandler` = `from ./anthropic`
- `AwsBedrockHandler` = `from ./bedrock`
- `CerebrasHandler` = `from ./cerebras`
- `ChutesHandler` = `from ./chutes`

---

### src\api\providers\io-intelligence.ts
**Purpose:** Manages API requests for IO Intelligence models, extending an OpenAI-compatible provider.

**Exported Functions:**
- `getModel(): { id: IOIntelligenceModelId; info: ModelInfo }` → `{ id: IOIntelligenceModelId; info: ModelInfo }`

**Exported Types:**
- `class IOIntelligenceHandler`: constructor(options: ApiHandlerOptions), getModel(): { id: IOIntelligenceModelId; info: ModelInfo }

**Key Imports:** `@roo-code/types`, `../../shared/api`, `./base-openai-compatible-provider`

---

### src\api\providers\lite-llm.ts
**Purpose:** Handles LiteLLM API requests, proxying to various LLM providers with OpenAI compatibility.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`

**Exported Types:**
- `class LiteLLMHandler`: constructor(options: ApiHandlerOptions), createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream

**Key Imports:** `openai`, `@anthropic-ai/sdk`, `@roo-code/types`, `../../shared/cost`, `../../shared/api`

---

### src\api\providers\lm-studio.ts
**Purpose:** Provides an API handler for LM Studio, supporting local LLM interactions.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`

**Exported Types:**
- `class LmStudioHandler`: constructor(options: ApiHandlerOptions), protected options: ApiHandlerOptions, private client: OpenAI, private readonly providerName: string

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `axios`, `@roo-code/types`, `../../shared/api`

---

### src\api\providers\mistral.ts
**Purpose:** Implements an API handler for Mistral models, including Codestral support.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`

**Exported Types:**
- `type ContentChunkWithThinking`: type: string, text?: string, thinking?: Array<{ type: string; text?: string }>
- `class MistralHandler`: constructor(options: ApiHandlerOptions), protected options: ApiHandlerOptions, private client: Mistral, createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream

**Key Imports:** `@anthropic-ai/sdk`, `@mistralai/mistralai`, `@roo-code/types`, `../../shared/api`, `../transform/mistral-format`

---

### src\api\providers\moonshot.ts
**Purpose:** Handles Moonshot API requests, extending the OpenAI handler with specific model and usage logic.

**Exported Functions:**
- `getModel(): { id: string; info: ModelInfo; [key: string]: any }` → `{ id: string; info: ModelInfo; [key: string]: any }`
- `processUsageMetrics(usage: any): ApiStreamUsageChunk` → `ApiStreamUsageChunk`

**Exported Types:**
- `class MoonshotHandler`: constructor(options: ApiHandlerOptions), getModel(): { id: string; info: ModelInfo; [key: string]: any }, processUsageMetrics(usage: any): ApiStreamUsageChunk

**Key Imports:** `openai`, `@roo-code/types`, `../../shared/api`, `../transform/stream`, `./openai`

---

### src\api\providers\native-ollama.ts
**Purpose:** Provides a native handler for Ollama API, converting messages to Ollama format.

**Exported Functions:**
- `convertToOllamaMessages(anthropicMessages: Anthropic.Messages.MessageParam[]): Message[]` → `Message[]`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`
- `fetchModel(): Promise<{ id: string; info: ModelInfo }>` → `Promise<{ id: string; info: ModelInfo }>`

**Exported Types:**
- `interface OllamaChatOptions`: temperature: number, num_ctx?: number
- `class NativeOllamaHandler`: constructor(options: ApiHandlerOptions), createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream, fetchModel(): Promise<{ id: string; info: ModelInfo }>

**Key Imports:** `@anthropic-ai/sdk`, `ollama`, `@roo-code/types`, `../transform/stream`, `./base-provider`

---

### src\api\providers\ollama.ts
**Purpose:** Implements an OpenAI-compatible API handler for Ollama, supporting local LLM instances.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`

**Exported Types:**
- `type CompletionUsage`: type: OpenAI.Chat.Completions.ChatCompletionChunk["usage"]
- `class OllamaHandler`: constructor(options: ApiHandlerOptions), protected options: ApiHandlerOptions, private client: OpenAI, private readonly providerName: string

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/openai-format`

---

### src\api\providers\openai-native.ts
**Purpose:** Provides a native handler for OpenAI API, including GPT-5 specific features.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`
- `getModel(): OpenAiNativeModel` → `OpenAiNativeModel`

**Exported Types:**
- `type OpenAiNativeModel`: type: ReturnType<OpenAiNativeHandler["getModel"]>
- `class OpenAiNativeHandler`: constructor(options: ApiHandlerOptions), protected options: ApiHandlerOptions, private client: OpenAI, private lastResponseId: string | undefined

**Exported Constants:**
- `GPT5_MODEL_PREFIX` = `"gpt-5"`

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../../shared/cost`

---

### src\api\providers\openai.ts
**Purpose:** Implements a general OpenAI-compatible API handler for various models and deployments.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`
- `getModel(): { id: string; info: ModelInfo; [key: string]: any }` → `{ id: string; info: ModelInfo; [key: string]: any }`

**Exported Types:**
- `class OpenAiHandler`: constructor(options: ApiHandlerOptions), protected options: ApiHandlerOptions, private client: OpenAI, private readonly providerName: string

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `axios`, `@roo-code/types`, `../../shared/api`

---

### src\api\providers\openrouter.ts
**Purpose:** Provides an API handler for OpenRouter, supporting diverse models and image generation.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): ApiStream` → `ApiStream`
- `fetchModel(): Promise<{ id: string; info: ModelInfo }>` → `Promise<{ id: string; info: ModelInfo }>`
- `getModel(): { id: string; info: ModelInfo; [key: string]: any }` → `{ id: string; info: ModelInfo; [key: string]: any }`
- `completePrompt(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata): Promise<OpenAI.Chat.Completions.ChatCompletion>` → `Promise<OpenAI.Chat.Completions.ChatCompletion>`

**Exported Types:**
- `interface ImageGenerationResponse`: choices?: Array<{ message?: { content?: string; images?: Array<{ type?: string; image_url?: { url?: string } }> } }>, error?: { message?: string; type?: string; code?: string }
- `class OpenRouterHandler`: constructor(options: ApiHandlerOptions), private client: OpenAI, private readonly providerName: string, private options: ApiHandlerOptions

**Key Imports:** `@anthropic-ai/sdk`, `openai`, `@roo-code/types`, `../../shared/api`, `../transform/openai-format`

---

### src\api\providers\qwen-code.ts
**Purpose:** Manages Qwen Code provider configuration, OAuth credentials, and API interaction setup.

**Exported Types:**
- `interface QwenOAuthCredentials`: access_token: string, refresh_token: string, token_type: string, expiry_date: number, resource_url?: string
- `interface QwenCodeHandlerOptions`: qwenCodeOauthPath?: string

**Exported Constants:**
- `QWEN_OAUTH_BASE_URL` = `"https://chat.qwen.ai"`
- `QWEN_OAUTH_TOKEN_ENDPOINT` = `"https://chat.qwen.ai/api/v1/oauth2/token"`
- `QWEN_OAUTH_CLIENT_ID` = `"f0304373b74a44d2b584a3fb70ca9e56"`
- `QWEN_DIR` = `".qwen"`
- `QWEN_CREDENTIAL_FILENAME` = `"oauth_creds.json"`

**Key Imports:** `@roo-code/types`, `node:fs`, `os`, `path`, `../../shared/api`

---

### src\api\providers\requesty.ts
**Purpose:** Defines the Requesty API handler, extending OpenAI parameters for tracing and usage reporting.

**Exported Types:**
- `interface RequestyUsage`: prompt_tokens_details?: { caching_tokens?: number, cached_tokens?: number }, total_cost?: number
- `type RequestyChatCompletionParams`: requesty?: { trace_id?: string, extra?: { mode?: string } }, thinking?: AnthropicReasoningParams
- `class RequestyHandler`

**Key Imports:** `@roo-code/types`, `openai`, `../../shared/api`, `../transform/stream`, `../transform/openai-format`

---

### src\api\providers\roo.ts
**Purpose:** Implements the Roo Code Cloud API handler, managing authentication state and model access.

**Exported Functions:**
- `dispose()` → `void`
- `getModel()` → `object`

**Exported Types:**
- `class RooHandler`

**Key Imports:** `@roo-code/types`, `@roo-code/cloud`, `openai`, `../../shared/api`, `./base-openai-compatible-provider`

---

### src\api\providers\router-provider.ts
**Purpose:** Provides an abstract base class for API providers that route requests using an OpenAI client.

**Exported Functions:**
- `fetchModel()` → `Promise<void>`

**Exported Types:**
- `type RouterProviderOptions`: name: RouterName, baseURL: string, apiKey?: string, modelId?: string, defaultModelId: string
- `class RouterProvider`: options: ApiHandlerOptions, name: RouterName, models: ModelRecord, client: OpenAI

**Key Imports:** `openai`, `@roo-code/types`, `../../shared/api`, `./base-provider`, `./fetchers/modelCache`

---

### src\api\providers\sambanova.ts
**Purpose:** Implements the SambaNova API handler using the OpenAI compatible provider base.

**Exported Types:**
- `class SambaNovaHandler`

**Key Imports:** `@roo-code/types`, `../../shared/api`, `./base-openai-compatible-provider`

---

### src\api\providers\unbound.ts
**Purpose:** Implements the Unbound API handler, managing caching metadata and custom request parameters.

**Exported Types:**
- `interface UnboundUsage`: cache_creation_input_tokens?: number, cache_read_input_tokens?: number
- `type UnboundChatCompletionCreateParamsStreaming`: unbound_metadata: { originApp: string, taskId?: string, mode?: string }
- `type UnboundChatCompletionCreateParamsNonStreaming`: unbound_metadata: { originApp: string }
- `class UnboundHandler`

**Exported Constants:**
- `ORIGIN_APP` = `"roo-code"`
- `DEFAULT_HEADERS` = `{ "X-Unbound-Metadata": JSON.stringify({ labels: [{ key: "app", value: "roo-code" }] }) }`

**Key Imports:** `@roo-code/types`, `openai`, `../../shared/api`, `../transform/stream`, `./router-provider`

---

### src\api\providers\utils\__tests__\timeout-config.spec.ts
---

### src\api\providers\utils\openai-error-handler.ts
**Purpose:** Handles and transforms technical OpenAI client errors into user-friendly messages.

**Exported Functions:**
- `handleOpenAIError(error: unknown, providerName: string)` → `Error`

**Key Imports:** `../../../i18n/setup`

---

### src\api\providers\utils\timeout-config.ts
**Purpose:** Retrieves and validates the configured API request timeout value in milliseconds.

**Exported Functions:**
- `getApiRequestTimeout()` → `number`

**Key Imports:** `vscode`

---

### src\api\providers\vercel-ai-gateway.ts
**Purpose:** Implements the Vercel AI Gateway handler, supporting streaming and caching metadata.

**Exported Functions:**
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`

**Exported Types:**
- `interface VercelAiGatewayUsage`: cache_creation_input_tokens?: number, cost?: number
- `class VercelAiGatewayHandler`

**Key Imports:** `@roo-code/types`, `openai`, `../../shared/api`, `../transform/stream`, `./router-provider`

---

### src\api\providers\vertex.ts
**Purpose:** Implements the Vertex AI handler, extending Gemini functionality and adjusting model parameters.

**Exported Functions:**
- `getModel()` → `object`

**Exported Types:**
- `class VertexHandler`

**Key Imports:** `@roo-code/types`, `../../shared/api`, `../transform/model-params`, `./gemini`, `../index`

---

### src\api\providers\vscode-lm.ts
**Purpose:** Handles chat completions using the VS Code Language Model API for integrated functionality.

**Exported Functions:**
- `getVsCodeLmModels()` → `Promise<ModelInfo[]>`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`

**Exported Types:**
- `class VsCodeLmHandler`

**Key Imports:** `vscode`, `@roo-code/types`, `../../shared/api`, `../transform/stream`, `../transform/vscode-lm-format`

---

### src\api\providers\xai.ts
**Purpose:** Implements the xAI API handler using an OpenAI compatible client configuration.

**Exported Functions:**
- `getModel()` → `object`
- `createMessage(systemPrompt: string, messages: Anthropic.Messages.MessageParam[], metadata?: ApiHandlerCreateMessageMetadata)` → `ApiStream`

**Exported Types:**
- `class XAIHandler`

**Exported Constants:**
- `XAI_DEFAULT_TEMPERATURE` = `0`

**Key Imports:** `@roo-code/types`, `openai`, `../../shared/api`, `../transform/stream`, `./base-provider`

---

### src\api\providers\zai.ts
**Purpose:** Implements the Z AI handler, configuring base URL and models based on API line selection.

**Exported Types:**
- `class ZAiHandler`

**Key Imports:** `@roo-code/types`, `../../shared/api`, `./base-openai-compatible-provider`

---

### src\api\transform\__tests__\bedrock-converse-format.spec.ts
---

### src\api\transform\__tests__\gemini-format.spec.ts
---

### src\api\transform\__tests__\image-cleaning.spec.ts
---

### src\api\transform\__tests__\mistral-format.spec.ts
---

### src\api\transform\__tests__\model-params.spec.ts
---

### src\api\transform\__tests__\openai-format.spec.ts
---

### src\api\transform\__tests__\r1-format.spec.ts
---

### src\api\transform\__tests__\reasoning.spec.ts
---

### src\api\transform\__tests__\simple-format.spec.ts
---

### src\api\transform\__tests__\stream.spec.ts
---

### src\api\transform\__tests__\vscode-lm-format.spec.ts
**Functions:** `constructor`

---

### src\api\transform\bedrock-converse-format.ts
**Purpose:** This file converts Anthropic messages to Bedrock Converse format.

**Exported Functions:**
- `convertToBedrockConverseMessages(anthropicMessages: Anthropic.Messages.MessageParam[])` → `Message[]`

**Key Imports:** `@anthropic-ai/sdk`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\transform\cache-strategy\__tests__\cache-strategy.spec.ts
**Functions:** `createMessageWithTokens`, `createMessage`, `logPlacements`, `mockResolvedValue`, `mockImplementation`, `await`

---

### src\api\transform\cache-strategy\base-strategy.ts
**Purpose:** This file defines the base class for cache strategy implementations.

**Exported Types:**
- `interface CacheStrategyConfig`
- `interface CacheResult`
- `interface CachePointPlacement`

**Key Imports:** `@anthropic-ai/sdk`, `@aws-sdk/client-bedrock-runtime`

---

### src\api\transform\cache-strategy\multi-point-strategy.ts
---

### src\api\transform\cache-strategy\types.ts
---

### src\api\transform\caching\__tests__\anthropic.spec.ts
---

### src\api\transform\caching\__tests__\gemini.spec.ts
---

### src\api\transform\caching\__tests__\vercel-ai-gateway.spec.ts
---

### src\api\transform\caching\__tests__\vertex.spec.ts
---

### src\api\transform\caching\anthropic.ts
**Functions:** `addCacheBreakpoints`

---

### src\api\transform\caching\gemini.ts
**Functions:** `addCacheBreakpoints`

---

### src\api\transform\caching\vercel-ai-gateway.ts
**Functions:** `addCacheBreakpoints`

---

### src\api\transform\caching\vertex.ts
**Functions:** `addCacheBreakpoints`, `cachedMessage`

---

### src\api\transform\gemini-format.ts
**Functions:** `convertAnthropicContentToGemini`, `convertAnthropicMessageToGemini`

---

### src\api\transform\image-cleaning.ts
**Functions:** `maybeRemoveImageBlocks`

---

### src\api\transform\mistral-format.ts
**Functions:** `convertToMistralMessages`

---

### src\api\transform\model-params.ts
**Functions:** `getModelParams`

---

### src\api\transform\openai-format.ts
**Purpose:** Converts Anthropic messages into the format required by OpenAI chat completions.

**Exported Functions:**
- `convertToOpenAiMessages(anthropicMessages: Anthropic.Messages.MessageParam[]): OpenAI.Chat.ChatCompletionMessageParam[]` → `OpenAI.Chat.ChatCompletionMessageParam[]`

**Key Imports:** `@anthropic-ai/sdk`, `openai`

---

### src\api\transform\r1-format.ts
**Purpose:** Converts Anthropic messages to R1 format, merging consecutive messages with the same role.

**Exported Functions:**
- `convertToR1Format(messages: AnthropicMessage[]): Message[]` → `Message[]`

**Exported Types:**
- `type ContentPartText`: OpenAI.Chat.ChatCompletionContentPartText
- `type ContentPartImage`: OpenAI.Chat.ChatCompletionContentPartImage
- `type UserMessage`: OpenAI.Chat.ChatCompletionUserMessageParam
- `type AssistantMessage`: OpenAI.Chat.ChatCompletionAssistantMessageParam
- `type Message`: OpenAI.Chat.ChatCompletionMessageParam
- `type AnthropicMessage`: Anthropic.Messages.MessageParam

**Key Imports:** `@anthropic-ai/sdk`, `openai`

---

### src\api\transform\reasoning.ts
**Purpose:** Calculates provider-specific reasoning parameters based on model capabilities and settings.

**Exported Functions:**
- `getOpenRouterReasoning({ model, reasoningBudget, reasoningEffort, settings }: GetModelReasoningOptions): OpenRouterReasoningParams | undefined` → `OpenRouterReasoningParams | undefined`
- `getAnthropicReasoning({ model, reasoningBudget, settings }: GetModelReasoningOptions): AnthropicReasoningParams | undefined` → `AnthropicReasoningParams | undefined`

**Exported Types:**
- `type OpenRouterReasoningParams`: effort, max_tokens, exclude
- `type AnthropicReasoningParams`: BetaThinkingConfigParam
- `type OpenAiReasoningParams`: reasoning_effort
- `type GeminiReasoningParams`: GenerateContentConfig["thinkingConfig"]
- `type GetModelReasoningOptions`: model, reasoningBudget, reasoningEffort, settings

**Key Imports:** `@anthropic-ai/sdk/resources/beta`, `openai`, `@google/genai`, `@roo-code/types`, `../../shared/api`

---

### src\api\transform\simple-format.ts
**Purpose:** Converts complex Anthropic message content into a simplified string format.

**Exported Functions:**
- `convertToSimpleContent(content: Anthropic.Messages.MessageParam["content"]): string` → `string`
- `convertToSimpleMessages(messages: Anthropic.Messages.MessageParam[]): Array<{ role: "user" | "assistant"; content: string }>` → `Array<{ role: "user" | "assistant"; content: string }>`

**Key Imports:** `@anthropic-ai/sdk`

---

### src\api\transform\stream.ts
**Purpose:** Defines the structure for streaming API responses across various chunk types.

**Exported Types:**
- `type ApiStream`: AsyncGenerator<ApiStreamChunk>
- `type ApiStreamChunk`: ApiStreamTextChunk, ApiStreamUsageChunk, ApiStreamReasoningChunk, ApiStreamGroundingChunk, ApiStreamError
- `interface ApiStreamError`: type, error, message
- `interface ApiStreamTextChunk`: type, text
- `interface ApiStreamReasoningChunk`: type, text
- `interface ApiStreamUsageChunk`: type, inputTokens, outputTokens, cacheWriteTokens, cacheReadTokens
- `interface ApiStreamGroundingChunk`: type, sources
- `interface GroundingSource`: title, url, snippet

---

### src\api\transform\vscode-lm-format.ts
**Purpose:** Converts Anthropic messages into the format compatible with VS Code Language Model API.

**Exported Functions:**
- `asObjectSafe(value: any): object` → `object`
- `convertToVsCodeLmMessages(anthropicMessages: Anthropic.Messages.MessageParam[]): vscode.LanguageModelChatMessage[]` → `vscode.LanguageModelChatMessage[]`

**Key Imports:** `@anthropic-ai/sdk`, `vscode`

---

### src\core\assistant-message\__tests__\AssistantMessageParser.spec.ts
**Functions:** `createSeededRandom`, `streamChunks`, `example`, `isEmptyTextContent`

---

### src\core\assistant-message\__tests__\parseAssistantMessage.spec.ts
**Functions:** `example`, `isEmptyTextContent`

---

### src\core\assistant-message\__tests__\parseAssistantMessageBenchmark.ts
**Functions:** `example`, `newFunction`, `runBenchmark`

---

### src\core\assistant-message\AssistantMessageParser.ts
**Functions:** `constructor`

---

### src\core\assistant-message\index.ts
---

### src\core\assistant-message\parseAssistantMessage.ts
**Functions:** `parseAssistantMessage`

---

### src\core\assistant-message\parseAssistantMessageV2.ts
**Functions:** `parseAssistantMessageV2`

---

### src\core\assistant-message\presentAssistantMessage.ts
**Functions:** `presentAssistantMessage`, `checkpointSaveAndMark`, `pushToolResult`, `askApproval`, `askFinishSubTaskApproval`, `handleError`

---

### src\core\checkpoints\__tests__\checkpoint.test.ts
---

### src\core\checkpoints\index.ts
**Functions:** `getCheckpointService`, `checkGitInstallation`, `checkpointSave`, `checkpointRestore`, `checkpointDiff`, `log`

---

### src\core\condense\__tests__\condense.spec.ts
---

### src\core\condense\__tests__\index.spec.ts
**Functions:** `return`

---

### src\core\condense\index.ts
**Functions:** `summarizeConversation`, `getMessagesSinceLastSummary`, `await`

---

### src\core\config\__tests__\ContextProxy.spec.ts
---

### src\core\config\__tests__\CustomModesManager.exportImportSlugChange.spec.ts
---

### src\core\config\__tests__\CustomModesManager.spec.ts
---

### src\core\config\__tests__\CustomModesManager.yamlEdgeCases.spec.ts
**Functions:** `mockFsReadFile`

---

### src\core\config\__tests__\CustomModesSettings.spec.ts
---

### src\core\config\__tests__\importExport.spec.ts
---

### src\core\config\__tests__\ModeConfig.spec.ts
**Functions:** `validateCustomMode`

---

### src\core\config\__tests__\ProviderSettingsManager.spec.ts
---

### src\core\config\ContextProxy.ts
**Purpose:** Manages VS Code extension context, global state, and secrets, providing cached access and migration utilities.

**Exported Functions:**
- `isPassThroughStateKey(key: string)` → `boolean`
- `isInitialized()` → `boolean`
- `initialize()` → `Promise<void>`
- `migrateImageGenerationSettings()` → `Promise<void>`
- `extensionUri()` → `vscode.Uri`
- `extensionPath()` → `string`
- `globalStorageUri()` → `vscode.Uri`
- `logUri()` → `vscode.Uri`
- `extension()` → `vscode.Extension<any>`
- `extensionMode()` → `vscode.ExtensionMode`
- `getSecret(key: GlobalSecretKey)` → `Promise<string | undefined>`
- `storeSecret(key: GlobalSecretKey, value: string)` → `Promise<void>`
- `setProviderSettings(settings: ProviderSettings)` → `Promise<void>`
- `setValues(values: Partial<RooCodeSettings>)` → `Promise<void>`
- `resetAllState()` → `Promise<void>`
- `instance()` → `ContextProxy`
- `getInstance()` → `ContextProxy`

**Exported Types:**
- `class ContextProxy`: constructor(context: vscode.ExtensionContext), isInitialized: boolean, extensionUri: vscode.Uri, getSecret(key: GlobalSecretKey): Promise<string | undefined>, setValues(values: Partial<RooCodeSettings>): Promise<void>

**Key Imports:** `vscode`, `@roo-code/types`, `zod`, `@roo-code/telemetry`, `../../utils/logging`

---

### src\core\config\CustomModesManager.ts
**Purpose:** Manages reading, writing, and caching custom mode configurations from workspace and global settings.

**Exported Types:**
- `interface RuleFile`: relativePath: string, content: string
- `interface ExportedModeConfig`: rulesFiles?: RuleFile[], slug: string, name: string, roleDefinition: string
- `interface ImportData`: customModes: ExportedModeConfig[]
- `interface ExportResult`: success: boolean, yaml?: string, error?: string
- `interface ImportResult`: success: boolean, error?: string
- `class CustomModesManager`: constructor(context: vscode.ExtensionContext), cachedModes: ModeConfig[] | null, cacheTTL: 10_000

**Key Imports:** `vscode`, `path`, `fs/promises`, `yaml`, `@roo-code/types`

---

### src\core\config\importExport.ts
**Purpose:** Handles importing and exporting extension configuration settings, including provider profiles and custom modes.

**Exported Functions:**
- `importSettingsFromPath(filePath: string, { providerSettingsManager, contextProxy, customModesManager }: ImportOptions)` → `Promise<void>`
- `importSettings()` → `Promise<void>`
- `importSettingsFromFile()` → `Promise<void>`
- `exportSettings(options: ExportOptions)` → `Promise<void>`
- `importSettingsWithFeedback(options: ImportWithProviderOptions)` → `Promise<void>`

**Exported Types:**
- `type ImportOptions`: providerSettingsManager: ProviderSettingsManager, contextProxy: ContextProxy, customModesManager: CustomModesManager
- `type ExportOptions`: providerSettingsManager: ProviderSettingsManager, contextProxy: ContextProxy
- `type ImportWithProviderOptions`: providerSettingsManager: ProviderSettingsManager, contextProxy: ContextProxy, provider: { settingsImportedAt?: number, postStateToWebview: () => Promise<void> }

**Key Imports:** `vscode`, `zod`, `@roo-code/types`, `./ProviderSettingsManager`, `./ContextProxy`

---

### src\core\config\ProviderSettingsManager.ts
**Purpose:** Manages storage, retrieval, and migration of AI provider configuration profiles using VS Code secrets.

**Exported Functions:**
- `generateId()` → `string`
- `initialize()` → `Promise<void>`
- `migrateRateLimitSeconds()` → `Promise<void>`
- `migrateDiffSettings()` → `Promise<void>`
- `migrateOpenAiHeaders()` → `Promise<void>`
- `migrateConsecutiveMistakeLimit()` → `Promise<void>`
- `migrateTodoListEnabled()` → `Promise<void>`
- `deleteConfig(id: string)` → `Promise<void>`
- `hasConfig(id: string)` → `boolean`
- `setModeConfig(mode: Mode, configId: string)` → `Promise<void>`
- `getModeConfigId(mode: Mode)` → `string | undefined`
- `export()` → `Promise<ProviderProfiles>`
- `import(profiles: ProviderProfiles)` → `Promise<void>`
- `resetAllConfigs()` → `Promise<void>`
- `secretsKey()` → `string`
- `store()` → `Promise<void>`

**Exported Types:**
- `interface SyncCloudProfilesResult`: hasChanges: boolean, activeProfileChanged: boolean, activeProfileId: string
- `class ProviderSettingsManager`: constructor(context: ExtensionContext), initialize(): Promise<void>, deleteConfig(id: string): Promise<void>, export(): Promise<ProviderProfiles>, secretsKey: string

**Key Imports:** `vscode`, `zod`, `@roo-code/types`, `fast-deep-equal`, `@roo-code/telemetry`

---

### src\core\context-tracking\FileContextTracker.ts
**Functions:** `constructor`, `setupFileWatcher`, `trackFileContext`, `saveTaskMetadata`, `addFileToFileContextTracker`

---

### src\core\context-tracking\FileContextTrackerTypes.ts
---

### src\core\context\context-management\__tests__\context-error-handling.test.ts
**Functions:** `status`

---

### src\core\context\context-management\context-error-handling.ts
**Purpose:** Checks if a given API error indicates the context window size was exceeded.

**Exported Functions:**
- `checkContextWindowExceededError(error: unknown)` → `boolean`

**Key Imports:** `openai`

---

### src\core\diff\insert-groups.ts
**Functions:** `insertGroups`

---

### src\core\diff\strategies\__tests__\multi-search-replace.spec.ts
**Functions:** `hello`, `helloWorld`, `example`, `test`, `one`, `two`, `three`, `four`, `five`, `getData`, `processUsers`, `handleItems`, `processData`, `sum`, `outer`, `toBe`, `constructor`, `getValue`, `method`

---

### src\core\diff\strategies\multi-file-search-replace.ts
**Functions:** `getSimilarity`, `fuzzySearch`, `reportMergeConflictError`, `reportInvalidDiffError`, `reportLineMarkerInReplaceError`, `constructor`

---

### src\core\diff\strategies\multi-search-replace.ts
**Functions:** `getSimilarity`, `fuzzySearch`, `reportMergeConflictError`, `reportInvalidDiffError`, `reportLineMarkerInReplaceError`, `constructor`

---

### src\core\environment\__tests__\getEnvironmentDetails.spec.ts
---

### src\core\environment\getEnvironmentDetails.ts
**Functions:** `getEnvironmentDetails`

---

### src\core\environment\reminder.ts
**Functions:** `formatReminderSection`

---

### src\core\ignore\__mocks__\RooIgnoreController.ts
**Functions:** `constructor`

---

### src\core\ignore\__tests__\RooIgnoreController.security.spec.ts
---

### src\core\ignore\__tests__\RooIgnoreController.spec.ts
---

### src\core\ignore\RooIgnoreController.ts
**Functions:** `constructor`

---

### src\core\mentions\__tests__\index.spec.ts
**Purpose:** Tests URL error handling for mention parsing functionality.

**Key Imports:** `vscode`, `../index`, `../../../services/browser/UrlContentFetcher`

---

### src\core\mentions\__tests__\processUserContentMentions.spec.ts
**Purpose:** Tests the processing of user content mentions with various parameters.

**Key Imports:** `../processUserContentMentions`, `../index`, `../../../services/browser/UrlContentFetcher`, `../../context-tracking/FileContextTracker`

---

### src\core\mentions\index.ts
**Functions:** `getUrlErrorMessage`, `openMention`, `parseMentions`, `getFileOrFolderContent`, `getWorkspaceProblems`, `getLatestTerminalOutput`

---

### src\core\mentions\processUserContentMentions.ts
**Functions:** `processUserContentMentions`, `shouldProcessMentions`

---

### src\core\message-queue\MessageQueueService.ts
**Purpose:** Manages a queue of messages with add, remove, and update functionalities.

**Exported Functions:**
- `constructor` → ``
- `addMessagetext: string, images?: string[]` → `QueuedMessage | undefined`
- `removeMessageid: string` → `boolean`
- `updateMessageid: string, text: string, images?: string[]` → `boolean`

**Exported Types:**
- `interface MessageQueueState`: messages: QueuedMessage[], isProcessing: boolean, isPaused: boolean
- `interface QueueEvents`: stateChanged: [messages: QueuedMessage[]]
- `class MessageQueueService`: _messages: QueuedMessage[], addMessage, removeMessage, updateMessage

**Key Imports:** `events`, `uuid`, `@roo-code/types`

---

### src\core\prompts\__tests__\add-custom-instructions.spec.ts
**Purpose:** Skips test file for adding custom instructions to system prompts.

**Key Imports:** `../system`, `../../../services/mcp/McpHub`, `../../../shared/modes`, `../../../utils/path`

---

### src\core\prompts\__tests__\custom-system-prompt.spec.ts
**Purpose:** Skips test file for custom system prompt generation logic.

**Key Imports:** `../system`, `../../../shared/modes`, `fs/promises`, `./utils`

---

### src\core\prompts\__tests__\get-prompt-component.spec.ts
**Purpose:** Skips test file for retrieving prompt components based on mode.

**Key Imports:** `@roo-code/types`, `../system`

---

### src\core\prompts\__tests__\responses-rooignore.spec.ts
**Purpose:** Skips test file for formatting responses related to .rooignore.

**Key Imports:** `../responses`, `../../ignore/RooIgnoreController`, `../../../utils/fs`, `fs/promises`, `./utils`

---

### src\core\prompts\__tests__\sections.spec.ts
**Purpose:** Skips test file for prompt section generation utilities.

**Key Imports:** `../sections/custom-instructions`, `../sections/capabilities`, `../../../shared/tools`

---

### src\core\prompts\__tests__\system-prompt.spec.ts
**Purpose:** Skips test file for core system prompt construction logic.

**Key Imports:** `../system`, `../../../services/mcp/McpHub`, `../../../shared/modes`

---

### src\core\prompts\__tests__\utils.ts
**Purpose:** Converts file paths to a consistent Unix-like (posix) format.

**Exported Functions:**
- `toPosix(filePath: PathLike | fs.FileHandle)` → `string`

**Key Imports:** `fs/promises`, `fs`

---

### src\core\prompts\instructions\create-mcp-server.ts
**Purpose:** Generates instructions for creating and configuring MCP servers.

**Exported Functions:**
- `createMCPServerInstructionsmcpHub: McpHub | undefined, diffStrategy: DiffStrategy | undefined` → `Promise<string>`

**Key Imports:** `../../../services/mcp/McpHub`, `../../../shared/tools`

---

### src\core\prompts\instructions\create-mode.ts
**Purpose:** Provides instructions for creating and managing custom modes in VS Code.

**Exported Functions:**
- `createModeInstructionscontext: vscode.ExtensionContext | undefined` → `Promise<string>`

**Key Imports:** `path`, `vscode`, `../../../shared/globalFileNames`

---

### src\core\prompts\instructions\instructions.ts
**Purpose:** Fetches instructions based on the provided text and details.

**Exported Functions:**
- `fetchInstructionstext: string, detail: InstructionsDetail` → `Promise<string>`

**Exported Types:**
- `interface InstructionsDetail`: mcpHub?: McpHub, diffStrategy?: DiffStrategy, context?: vscode.ExtensionContext

**Key Imports:** `./create-mcp-server`, `./create-mode`, `../../../services/mcp/McpHub`, `../../../shared/tools`, `vscode`

---

### src\core\prompts\responses.ts
**Purpose:** Defines various response formats for tool interactions and errors.

**Exported Constants:**
- `formatResponse` = `string`

**Key Imports:** `@anthropic-ai/sdk`, `path`, `diff`, `../ignore/RooIgnoreController`, `../protect/RooProtectedController`

---

### src\core\prompts\sections\__tests__\custom-instructions-global.spec.ts
---

### src\core\prompts\sections\__tests__\custom-instructions-path-detection.spec.ts
---

### src\core\prompts\sections\__tests__\custom-instructions.spec.ts
---

### src\core\prompts\sections\__tests__\custom-system-prompt.spec.ts
---

### src\core\prompts\sections\__tests__\objective.spec.ts
---

### src\core\prompts\sections\__tests__\tool-use-guidelines.spec.ts
---

### src\core\prompts\sections\capabilities.ts
**Purpose:** Generates a section describing the available capabilities and tools.

**Exported Functions:**
- `getCapabilitiesSectioncwd: string, supportsComputerUse: boolean, mcpHub?: McpHub, diffStrategy?: DiffStrategy, codeIndexManager?: CodeIndexManager` → `string`

**Key Imports:** `../../../shared/tools`, `../../../services/mcp/McpHub`, `../../../services/code-index/manager`

---

### src\core\prompts\sections\custom-instructions.ts
**Purpose:** Provides functions for reading and processing custom instructions.

**Exported Functions:**
- `safeReadFilefilePath: string` → `Promise<string>`
- `directoryExistsdirPath: string` → `Promise<boolean>`
- `resolveDirectoryEntryentry: Dirent, dirPath: string, fileInfo: Array<{ originalPath: string; resolvedPath: string }>, depth: number` → `Promise<void>`
- `resolveSymLinkentry: Dirent, dirPath: string, fileInfo: Array<{ originalPath: string; resolvedPath: string }>, depth: number` → `Promise<void>`
- `readTextFilesFromDirectorydirPath: string, fileInfo: Array<{ originalPath: string; resolvedPath: string }>, depth: number` → `Promise<void>`
- `formatDirectoryContentfileInfo: Array<{ originalPath: string; resolvedPath: string }>, cwd: string` → `string`
- `loadRuleFilesrooDir: string, ruleType: string` → `Promise<string[]>`
- `loadAgentRulesFilerooDir: string` → `Promise<string>`
- `addCustomInstructionscustomInstructions: string, prompt: string` → `string`
- `shouldIncludeRuleFilefilePath: string, ruleType: string` → `boolean`

**Exported Constants:**
- `MAX_DEPTH` = `5`

**Key Imports:** `fs`, `path`, `os`, `fs`, `@roo-code/types`, `../../../shared/language`, `../../../services/roo-config`

---

### src\core\prompts\sections\custom-system-prompt.ts
**Purpose:** Manages custom system prompts by interpolating variables and reading files.

**Exported Functions:**
- `interpolatePromptContentcontent: string, variables: PromptVariables` → `string`
- `safeReadFilefilePath: string` → `Promise<string>`
- `getSystemPromptFilePathcwd: string, mode: Mode` → `string`
- `loadSystemPromptFilefilePath: string` → `Promise<string>`
- `ensureRooDirectorycwd: string` → `Promise<void>`

**Exported Types:**
- `type PromptVariables`

**Key Imports:** `fs`, `path`, `../../../shared/modes`, `../../../utils/fs`

---

### src\core\prompts\sections\index.ts
**Purpose:** Exports various prompt section modules for modularity.

---

### src\core\prompts\sections\markdown-formatting.ts
**Purpose:** Generates a section with markdown formatting rules for responses.

**Exported Functions:**
- `markdownFormattingSection` → `string`

---

### src\core\prompts\sections\mcp-servers.ts
**Purpose:** Generates a section describing connected MCP servers and their tools.

**Exported Functions:**
- `getMcpServersSectionmcpHub?: McpHub, diffStrategy?: DiffStrategy, enableMcpServerCreation?: boolean` → `Promise<string>`

**Key Imports:** `../../../shared/tools`, `../../../services/mcp/McpHub`

---

### src\core\prompts\sections\modes.ts
**Purpose:** Provides a section detailing available modes and their descriptions.

**Exported Functions:**
- `getModesSectioncontext: vscode.ExtensionContext` → `Promise<string>`

**Key Imports:** `path`, `vscode`, `fs`, `../../../shared/modes`

---

### src\core\prompts\sections\objective.ts
**Purpose:** Generates the objective section for the prompt, outlining task goals.

**Exported Functions:**
- `getObjectiveSectioncodeIndexManager?: CodeIndexManager, experimentsConfig?: Record<string, boolean>` → `string`

**Key Imports:** `../../../services/code-index/manager`

---

### src\core\prompts\sections\rules.ts
**Purpose:** Provides editing instructions and rules for tool usage.

**Exported Functions:**
- `getEditingInstructionsdiffStrategy?: DiffStrategy` → `string`
- `getRulesSectioncwd: string, codeIndexManager?: CodeIndexManager, diffStrategy?: DiffStrategy` → `string`

**Key Imports:** `../../../shared/tools`, `../../../services/code-index/manager`

---

### src\core\prompts\sections\system-info.ts
**Purpose:** Defines a function that generates a system information section for prompts.

**Exported Functions:**
- `getSystemInfoSectioncwd: string` → `string`

**Key Imports:** `os`, `os-name`, `../../../utils/shell`

---

### src\core\prompts\sections\tool-use-guidelines.ts
**Purpose:** Defines a function that generates tool use guidelines section for prompts.

**Exported Functions:**
- `getToolUseGuidelinesSectioncodeIndexManager?: CodeIndexManager` → `string`

**Key Imports:** `../../../services/code-index/manager`

---

### src\core\prompts\sections\tool-use.ts
**Purpose:** Defines a function that returns a shared tool use section for prompts.

**Exported Functions:**
- `getSharedToolUseSection` → `string`

---

### src\core\prompts\system.ts
**Functions:** `getPromptComponent`, `generatePrompt`

---

### src\core\prompts\tools\__tests__\attempt-completion.spec.ts
---

### src\core\prompts\tools\__tests__\fetch-instructions.spec.ts
**Purpose:** Skips test file for fetch instructions description generation.

**Key Imports:** `../fetch-instructions`

---

### src\core\prompts\tools\__tests__\new-task.spec.ts
**Purpose:** Skips test file for new task description generation logic.

**Key Imports:** `../new-task`, `../types`

---

### src\core\prompts\tools\access-mcp-resource.ts
**Purpose:** Defines a function that generates the description for access_mcp_resource tool.

**Exported Functions:**
- `getAccessMcpResourceDescriptionargs: ToolArgs` → `string | undefined`

**Key Imports:** `./types`

---

### src\core\prompts\tools\ask-followup-question.ts
**Purpose:** Defines a function that generates the description for ask_followup_question tool.

**Exported Functions:**
- `getAskFollowupQuestionDescription` → `string`

---

### src\core\prompts\tools\attempt-completion.ts
**Purpose:** Defines a function that generates the description for attempt_completion tool.

**Exported Functions:**
- `getAttemptCompletionDescriptionargs?: ToolArgs` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\browser-action.ts
**Purpose:** Defines a function that generates the description for browser_action tool.

**Exported Functions:**
- `getBrowserActionDescriptionargs: ToolArgs` → `string | undefined`

**Key Imports:** `./types`

---

### src\core\prompts\tools\codebase-search.ts
**Purpose:** Defines a function that generates the description for codebase_search tool.

**Exported Functions:**
- `getCodebaseSearchDescriptionargs: ToolArgs` → `string`

**Key Imports:** `./types`

---

### src\core\prompts\tools\execute-command.ts
**Purpose:** Defines a function that generates the description for execute_command tool.

**Exported Functions:**
- `getExecuteCommandDescriptionargs: ToolArgs` → `string | undefined`

**Key Imports:** `./types`

---

### src\core\prompts\tools\fetch-instructions.ts
**Functions:** `getFetchInstructionsDescription`

---

### src\core\prompts\tools\generate-image.ts
**Functions:** `getGenerateImageDescription`

---

### src\core\prompts\tools\index.ts
**Functions:** `getToolDescriptionsForMode`

---

### src\core\prompts\tools\insert-content.ts
**Functions:** `getInsertContentDescription`

---

### src\core\prompts\tools\list-code-definition-names.ts
**Functions:** `getListCodeDefinitionNamesDescription`

---

### src\core\prompts\tools\list-files.ts
**Functions:** `getListFilesDescription`

---

### src\core\prompts\tools\new-task.ts
**Functions:** `getNewTaskDescription`

---

### src\core\prompts\tools\read-file.ts
**Functions:** `getReadFileDescription`

---

### src\core\prompts\tools\run-slash-command.ts
**Functions:** `getRunSlashCommandDescription`

---

### src\core\prompts\tools\search-and-replace.ts
**Functions:** `getSearchAndReplaceDescription`

---

### src\core\prompts\tools\search-files.ts
**Functions:** `getSearchFilesDescription`

---

### src\core\prompts\tools\simple-read-file.ts
**Functions:** `getSimpleReadFileDescription`

---

### src\core\prompts\tools\switch-mode.ts
**Functions:** `getSwitchModeDescription`

---

### src\core\prompts\tools\types.ts
---

### src\core\prompts\tools\update-todo-list.ts
**Functions:** `getUpdateTodoListDescription`

---

### src\core\prompts\tools\use-mcp-tool.ts
**Functions:** `getUseMcpToolDescription`

---

### src\core\prompts\tools\write-to-file.ts
**Functions:** `getWriteToFileDescription`

---

### src\core\prompts\types.ts
**Purpose:** Defines TypeScript interfaces for system prompt configuration settings.

**Exported Types:**
- `interface SystemPromptSettings`: maxConcurrentFileReads, todoListEnabled, useAgentRules, newTaskRequireTodos

---

### src\core\protect\__tests__\RooProtectedController.spec.ts
**Purpose:** Skips test file for the RooProtectedController write protection logic.

**Key Imports:** `path`, `../RooProtectedController`

---

### src\core\protect\RooProtectedController.ts
**Purpose:** Controls write access to sensitive Roo configuration files using ignore patterns.

**Exported Functions:**
- `isWriteProtected(filePath: string)` → `boolean`

**Exported Types:**
- `class RooProtectedController`: cwd, ignoreInstance, PROTECTED_PATTERNS

**Exported Constants:**
- `SHIELD_SYMBOL` = `"\u{1F6E1}"`

**Key Imports:** `path`, `ignore`

---

### src\core\sliding-window\__tests__\sliding-window.spec.ts
**Purpose:** Skips test file for sliding window token estimation and truncation logic.

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/types`, `@roo-code/telemetry`, `../../../api/providers/base-provider`, `../../task-persistence/apiMessages`, `../../condense`

---

### src\core\sliding-window\index.ts
**Purpose:** Manages conversation history size by estimating tokens and truncating messages.

**Exported Functions:**
- `estimateTokenCount(content: Array<Anthropic.Messages.ContentBlockParam>, apiHandler: ApiHandler)` → `Promise<number>`
- `truncateConversation(messages: ApiMessage[], fracToRemove: number)` → `ApiMessage[]`
- `truncateConversationIfNeeded(messages: ApiMessage[], apiHandler: ApiHandler, maxTokens: number)` → `Promise<{ truncatedMessages: ApiMessage[]; wasTruncated: boolean }>`

**Exported Constants:**
- `TOKEN_BUFFER_PERCENTAGE` = `0.1`

**Key Imports:** `@anthropic-ai/sdk`, `@roo-code/telemetry`, `../../api`, `../condense`, `../task-persistence/apiMessages`, `@roo-code/types`

---

### src\core\task-persistence\apiMessages.ts
**Functions:** `readApiMessages`, `saveApiMessages`

---

### src\core\task-persistence\index.ts
---

### src\core\task-persistence\taskMessages.ts
**Functions:** `readTaskMessages`, `saveTaskMessages`

---

### src\core\task-persistence\taskMetadata.ts
**Functions:** `taskMetadata`

---

### src\core\task\__tests__\AutoApprovalHandler.spec.ts
---

### src\core\task\__tests__\grounding-sources.test.ts
---

### src\core\task\__tests__\Task.dispose.test.ts
---

### src\core\task\__tests__\Task.spec.ts
**Functions:** `next`, `return`, `throw`

---

### src\core\task\AutoApprovalHandler.ts
**Purpose:** Handles automatic approval checks for API requests based on limits.

**Exported Functions:**
- `checkAutoApprovalLimits(state: GlobalState | undefined, messages: ClineMessage[], askForApproval: (type: ClineAsk, data: string) => Promise<{ response: ClineAskResponse; text?: string; images?: string[] }>)` → `Promise<AutoApprovalResult>`

**Exported Types:**
- `class AutoApprovalHandler`: lastResetMessageIndex, consecutiveAutoApprovedRequestsCount, consecutiveAutoApprovedCost

**Key Imports:** `@roo-code/types`, `../../shared/getApiMetrics`, `../../shared/WebviewMessage`

---

### src\core\task\Task.ts
**Purpose:** Manages the lifecycle, state, conversation, and persistence of a task.

**Exported Types:**
- `type TaskStatus`

**Key Imports:** `path`, `vscode`, `os`, `crypto`, `events`, `@anthropic-ai/sdk`, `delay`, `p-wait-for`, `serialize-error`, `@roo-code/types`, `@roo-code/telemetry`, `@roo-code/cloud`, `../../api`, `../../api/transform/stream`, `../../api/transform/image-cleaning`, `../../shared/array`, `../../shared/combineApiRequests`, `../../shared/combineCommandSequences`, `../../i18n`

---

### src\core\task\types.ts
---

### src\core\tools\__tests__\applyDiffTool.experiment.spec.ts
---

### src\core\tools\__tests__\askFollowupQuestionTool.spec.ts
---

### src\core\tools\__tests__\attemptCompletionTool.spec.ts
---

### src\core\tools\__tests__\executeCommand.spec.ts
**Functions:** `describe`

---

### src\core\tools\__tests__\executeCommandTimeout.integration.spec.ts
---

### src\core\tools\__tests__\executeCommandTool.spec.ts
---

### src\core\tools\__tests__\generateImageTool.test.ts
---

### src\core\tools\__tests__\insertContentTool.spec.ts
**Functions:** `executeInsertContentTool`, `toPosix`, `initialize`, `validateAccess`, `mockImplementation`

---

### src\core\tools\__tests__\multiApplyDiffTool.spec.ts
**Functions:** `instance`

---

### src\core\tools\__tests__\newTaskTool.spec.ts
---

### src\core\tools\__tests__\readFileTool.spec.ts
**Purpose:** Tests the functionality of the readFileTool using mocks and assertions.

**Exported Functions:**
- `initialize` → `any`
- `validateAccess` → `any`

**Key Imports:** `path`, `../../../integrations/misc/line-counter`, `../../../integrations/misc/read-lines`, `../../../integrations/misc/extract-text`, `../../../shared/tools`, `../readFileTool`

---

### src\core\tools\__tests__\runSlashCommandTool.spec.ts
**Purpose:** Tests the runSlashCommandTool, focusing on parameter handling and errors.

**Key Imports:** `vitest`, `../runSlashCommandTool`, `../../task/Task`, `../../prompts/responses`, `../../../services/command/commands`

---

### src\core\tools\__tests__\ToolRepetitionDetector.spec.ts
**Purpose:** Tests the ToolRepetitionDetector, ensuring correct repetition detection.

**Exported Functions:**
- `createToolUsename: string, displayName?: string, params: Record<string, string> = {}` → `ToolUse`

**Exported Types:**
- `class ToolRepetitionDetector`: check, reset, toolRepetitionLimit

**Key Imports:** `@roo-code/types`, `../../../shared/tools`, `../ToolRepetitionDetector`

---

### src\core\tools\__tests__\updateTodoListTool.spec.ts
**Purpose:** Tests parsing of Markdown checklists into TodoItem objects.

**Exported Functions:**
- `parseMarkdownChecklistmd: string` → `TodoItem[]`

**Key Imports:** `vitest`, `../updateTodoListTool`, `@roo-code/types`

---

### src\core\tools\__tests__\useMcpToolTool.spec.ts
**Purpose:** Tests the useMcpToolTool, focusing on error and result formatting.

**Key Imports:** `../useMcpToolTool`, `../../task/Task`, `../../../shared/tools`

---

### src\core\tools\__tests__\validateToolUse.spec.ts
**Purpose:** Tests tool use validation against different modes and tool groups.

**Key Imports:** `@roo-code/types`, `../../../shared/modes`, `../../../shared/tools`, `../validateToolUse`

---

### src\core\tools\__tests__\writeToFileTool.spec.ts
**Purpose:** Tests the writeToFileTool, including file access and path resolution.

**Exported Functions:**
- `initialize` → `any`
- `validateAccess` → `any`

**Key Imports:** `path`, `../../../utils/fs`, `../../../integrations/editor/detect-omission`, `../../../utils/pathUtils`, `../../../utils/path`, `../../../utils/text-normalization`, `../../../integrations/misc/extract-text`, `../../../shared/tools`, `../writeToFileTool`

---

### src\core\tools\accessMcpResourceTool.ts
**Functions:** `accessMcpResourceTool`

---

### src\core\tools\applyDiffTool.ts
**Functions:** `applyDiffToolLegacy`

---

### src\core\tools\askFollowupQuestionTool.ts
**Functions:** `askFollowupQuestionTool`

---

### src\core\tools\attemptCompletionTool.ts
**Functions:** `attemptCompletionTool`

---

### src\core\tools\browserActionTool.ts
**Functions:** `browserActionTool`

---

### src\core\tools\codebaseSearchTool.ts
**Functions:** `codebaseSearchTool`

---

### src\core\tools\executeCommandTool.ts
**Functions:** `executeCommandTool`, `executeCommand`

---

### src\core\tools\fetchInstructionsTool.ts
**Purpose:** Implements the fetchInstructions tool to retrieve and present task instructions.

**Exported Functions:**
- `fetchInstructionsTool(cline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult)` → `Promise<void>`

**Key Imports:** `../task/Task`, `../prompts/instructions/instructions`, `../../shared/ExtensionMessage`, `../prompts/responses`, `../../shared/tools`

---

### src\core\tools\generateImageTool.ts
**Purpose:** Executes the generateImage tool to create images using specified models.

**Exported Functions:**
- `generateImageTool(cline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag)` → `Promise<void>`

**Exported Constants:**
- `IMAGE_GENERATION_MODELS` = `["google/gemini-2.5-flash-image-preview"]`

**Key Imports:** `path`, `fs/promises`, `vscode`, `../task/Task`, `../../shared/tools`

---

### src\core\tools\helpers\imageHelpers.ts
**Purpose:** Defines constants and types for validating and handling image files during processing.

**Exported Types:**
- `interface ImageValidationResult`: isValid: boolean, reason?: "size_limit" | "memory_limit" | "unsupported_model", notice?: string

**Exported Constants:**
- `DEFAULT_MAX_IMAGE_FILE_SIZE_MB` = `5`
- `DEFAULT_MAX_TOTAL_IMAGE_SIZE_MB` = `20`
- `SUPPORTED_IMAGE_FORMATS` = `[ ".png", ".jpg", ".jpeg", ".gif", ".webp", ".svg", ".bmp", ".ico", ".tiff", ".tif", ".avif" ]`
- `IMAGE_MIME_TYPES` = `{ ".png": "image/png", ".jpg": "image/jpeg", ".jpeg": "image/jpeg", ".gif": "image/gif", ".webp": "image/webp", ".svg": "image/svg+xml", ".bmp": "image/bmp", ".ico": "image/x-icon", ".tiff": "image/tiff", ".tif": "image/tiff", ".avif": "image/avif" }`

**Key Imports:** `path`, `fs/promises`, `pretty-bytes`, `../../../i18n`

---

### src\core\tools\insertContentTool.ts
**Purpose:** Implements the insertContent tool to add content into a file at a specified line.

**Exported Functions:**
- `insertContentTool(cline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag)` → `Promise<void>`

**Key Imports:** `fs/promises`, `path`, `../../utils/path`, `../task/Task`, `../../shared/tools`

---

### src\core\tools\listCodeDefinitionNamesTool.ts
**Purpose:** Executes the tool to list top-level code definition names within a specified file.

**Exported Functions:**
- `listCodeDefinitionNamesTool(cline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag)` → `Promise<void>`

**Key Imports:** `path`, `fs/promises`, `../../shared/tools`, `../task/Task`, `../../services/tree-sitter`

---

### src\core\tools\listFilesTool.ts
**Purpose:** Implements the listFiles tool to recursively list files in a directory path.

**Exported Functions:**
- `listFilesTool(cline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag)` → `Promise<void>`

**Key Imports:** `path`, `../task/Task`, `../../shared/ExtensionMessage`, `../../services/glob/list-files`, `../../shared/tools`

---

### src\core\tools\multiApplyDiffTool.ts
**Purpose:** Defines data structures for parsing and tracking results of multi-file diff operations.

**Exported Types:**
- `interface DiffOperation`: path: string, diff: Array<{ content: string; startLine?: number }>
- `interface OperationResult`: path: string, status: "pending" | "approved" | "denied" | "blocked" | "error", error?: string, result?: string, diffItems?: Array<{ content: string; startLine?: number }>
- `interface ParsedFile`: path: string, diff: ParsedDiff | ParsedDiff[]
- `interface ParsedDiff`: content: string, start_line?: string
- `interface ParsedXmlResult`: file: ParsedFile | ParsedFile[]

**Key Imports:** `path`, `fs/promises`, `@roo-code/telemetry`, `../../shared/tools`, `../task/Task`

---

### src\core\tools\newTaskTool.ts
**Purpose:** Implements the newTask tool to create a new task with a specified mode and message.

**Exported Functions:**
- `newTaskTool(task: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag)` → `Promise<void>`

**Key Imports:** `vscode`, `@roo-code/types`, `../../shared/tools`, `../task/Task`, `../../shared/modes`

---

### src\core\tools\readFileTool.ts
**Purpose:** Provides the implementation for the readFile tool, handling content extraction and validation.

**Exported Functions:**
- `getReadFileToolDescription(blockName: string, blockParams: any)` → `string`

**Key Imports:** `path`, `isbinaryfile`, `../task/Task`, `../../shared/tools`, `./helpers/imageHelpers`

---

### src\core\tools\runSlashCommandTool.ts
**Purpose:** Executes the runSlashCommand tool to invoke internal slash commands.

**Exported Functions:**
- `runSlashCommandTool(task: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag)` → `Promise<void>`

**Key Imports:** `../task/Task`, `../../shared/tools`, `../prompts/responses`, `../../services/command/commands`, `../../shared/experiments`

---

### src\core\tools\searchAndReplaceTool.ts
**Purpose:** Implements the searchAndReplace tool for modifying file content using regex patterns.

**Key Imports:** `path`, `fs/promises`, `delay`, `../task/Task`, `../../shared/tools`

---

### src\core\tools\searchFilesTool.ts
**Purpose:** Executes the searchFiles tool to perform regex searches across the workspace using ripgrep.

**Exported Functions:**
- `searchFilesTool(cline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag)` → `Promise<void>`

**Key Imports:** `path`, `../task/Task`, `../../shared/tools`, `../../shared/ExtensionMessage`, `../../services/ripgrep`

---

### src\core\tools\simpleReadFileTool.ts
**Purpose:** Provides a simplified readFile tool implementation for models requiring single file access.

**Exported Functions:**
- `simpleReadFileTool(cline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag)` → `Promise<void>`

**Key Imports:** `path`, `isbinaryfile`, `../task/Task`, `../../shared/tools`, `./helpers/imageHelpers`

---

### src\core\tools\switchModeTool.ts
**Purpose:** Implements the switchMode tool to change the current operational mode of the task.

**Exported Functions:**
- `switchModeTool(cline: Task, block: ToolUse, askApproval: AskApproval, handleError: HandleError, pushToolResult: PushToolResult, removeClosingTag: RemoveClosingTag)` → `Promise<void>`

**Key Imports:** `delay`, `../task/Task`, `../../shared/tools`, `../prompts/responses`, `../../shared/modes`

---

### src\core\tools\ToolRepetitionDetector.ts
**Functions:** `constructor`

---

### src\core\tools\updateTodoListTool.ts
**Functions:** `addTodoToTask`, `updateTodoStatusForTask`, `removeTodoFromTask`, `getTodoListForTask`, `setTodoListForTask`, `restoreTodoListForTask`, `todoListToMarkdown`, `normalizeStatus`, `parseMarkdownChecklist`, `setPendingTodoList`, `validateTodos`, `updateTodoListTool`

---

### src\core\tools\useMcpToolTool.ts
**Functions:** `handlePartialRequest`, `validateParams`, `validateToolExists`, `sendExecutionStatus`, `processToolContent`, `executeToolAndProcessResult`, `useMcpToolTool`

---

### src\core\tools\validateToolUse.ts
**Functions:** `validateToolUse`

---

### src\core\tools\writeToFileTool.ts
**Functions:** `writeToFileTool`

---

### src\core\webview\__tests__\checkpointRestoreHandler.spec.ts
**Purpose:** Tests the checkpoint restore handler's functionality.

**Key Imports:** `vitest`, `../checkpointRestoreHandler`, `../../task-persistence`, `p-wait-for`, `vscode`

---

### src\core\webview\__tests__\ClineProvider.spec.ts
**Functions:** `delayFn`, `getMessageHandler`, `constructor`, `instance`

---

### src\core\webview\__tests__\ClineProvider.sticky-mode.spec.ts
**Functions:** `instance`

---

### src\core\webview\__tests__\messageEnhancer.test.ts
---

### src\core\webview\__tests__\telemetrySettingsTracking.spec.ts
---

### src\core\webview\__tests__\webviewMessageHandler.checkpoint.spec.ts
---

### src\core\webview\__tests__\webviewMessageHandler.delete.spec.ts
---

### src\core\webview\__tests__\webviewMessageHandler.edit.spec.ts
---

### src\core\webview\__tests__\webviewMessageHandler.spec.ts
---

### src\core\webview\checkpointRestoreHandler.ts
**Purpose:** Handles checkpoint restoration for deleting and editing operations.

**Exported Functions:**
- `handleCheckpointRestoreOperationconfig: CheckpointRestoreConfig` → `Promise<void>`
- `waitForClineInitialization` → `any`

**Exported Types:**
- `interface CheckpointRestoreConfig`: provider, currentCline, messageTs, messageIndex, checkpoint

**Key Imports:** `../task/Task`, `../webview/ClineProvider`, `../task-persistence`, `vscode`, `p-wait-for`, `../../i18n`

---

### src\core\webview\ClineProvider.ts
**Purpose:** Manages the webview, tasks, and communication with the UI.

**Exported Types:**
- `class ClineProvider`: onTaskStarted, onTaskCompleted, onTaskAborted, resolveWebviewView, postMessageToWebview, cwd

**Key Imports:** `os`, `path`, `fs`, `EventEmitter`, `@anthropic-ai/sdk`, `delay`, `axios`, `pWaitFor`, `vscode`, `@roo-code/types`, `@roo-code/telemetry`, `@roo-code/cloud`, `../../shared/package`

---

### src\core\webview\generateSystemPrompt.ts
**Purpose:** Generates system prompts based on provider state and webview messages.

**Exported Functions:**
- `generateSystemPromptprovider: ClineProvider, message: WebviewMessage` → `Promise<any>`

**Key Imports:** `vscode`, `../../shared/WebviewMessage`, `../../shared/modes`, `../../api`, `../../shared/experiments`, `../prompts/system`, `../diff/strategies/multi-search-replace`, `../diff/strategies/multi-file-search-replace`, `../webview/ClineProvider`

---

### src\core\webview\getNonce.ts
**Purpose:** Generates a unique alphanumeric identifier for content security.

**Exported Functions:**
- `getNonce` → `string`

---

### src\core\webview\getUri.ts
**Purpose:** Gets the webview URI for a given file or resource.

**Exported Functions:**
- `getUriwebview: Webview, extensionUri: Uri, pathList: string[]` → `Uri`

**Key Imports:** `vscode`

---

### src\core\webview\messageEnhancer.ts
**Purpose:** Enhances message prompts using AI, optionally including task history.

**Exported Types:**
- `interface MessageEnhancerOptions`: text, apiConfiguration, customSupportPrompts, listApiConfigMeta, enhancementApiConfigId
- `interface MessageEnhancerResult`: success, enhancedText, error
- `class MessageEnhancer`: enhanceMessage

**Key Imports:** `@roo-code/types`, `@roo-code/telemetry`, `../../shared/support-prompt`, `../../utils/single-completion-handler`, `../config/ProviderSettingsManager`, `./ClineProvider`

---

### src\core\webview\webviewMessageHandler.ts
**Purpose:** Handles messages from the webview, managing tasks and state.

**Exported Functions:**
- `webviewMessageHandlerprovider: ClineProvider, message: WebviewMessage` → `Promise<void>`
- `getCurrentCwdprovider: ClineProvider` → `Promise<string>`
- `findMessageIndicesmessages: ClineMessage[], messageTs: number` → `number[]`
- `findFirstApiIndexAtOrAftermessages: ClineMessage[], messageTs: number` → `number | undefined`
- `removeMessagesThisAndSubsequentmessages: ClineMessage[], startIndex: number` → `void`

**Key Imports:** `../../utils/safeWriteJson`, `path`, `os`, `fs`, `pWaitFor`, `vscode`, `@roo-code/types`, `@roo-code/cloud`, `@roo-code/telemetry`, `../task-persistence/apiMessages`, `../task-persistence`, `./ClineProvider`, `./checkpointRestoreHandler`, `../../i18n`, `../../shared/package`, `../../shared/api`, `./messageEnhancer`, `../../shared/WebviewMessage`, `../../shared/checkExistApiConfig`, `../../shared/experiments`, `../../integrations/terminal/Terminal`, `../../integrations/misc/open-file`, `../../integrations/misc/image-handler`, `../../integrations/misc/image-handler`

---

### src\extension.ts
**Purpose:** Activates the extension, registers providers, and initializes services and configurations.

**Exported Functions:**
- `activate(context: vscode.ExtensionContext)` → `Promise<void>`
- `deactivate()` → `Promise<void>`
- `postStateListener(context: vscode.ExtensionContext)` → `void`
- `debouncedReload(context: vscode.ExtensionContext)` → `void`

**Key Imports:** `vscode`, `@roo-code/cloud`, `@roo-code/telemetry`, `@dotenvx/dotenvx`, `@roo-code/types`

---

### src\extension\api.ts
**Purpose:** Exposes the RooCode API for extensions to interact with the ClineProvider.

**Exported Functions:**
- `constructor(outputChannel: vscode.OutputChannel, provider: ClineProvider, socketPath?: string, enableLogging = false)` → `void`
- `startNewTask(options?: CreateTaskOptions)` → `Promise<string>`
- `getCurrentTaskStack()` → `string[]`
- `clearCurrentTask()` → `Promise<void>`
- `cancelCurrentTask()` → `Promise<void>`
- `cancelTask(taskId: string)` → `Promise<void>`
- `sendMessage(message: any)` → `Promise<void>`
- `pressPrimaryButton()` → `Promise<void>`
- `pressSecondaryButton()` → `Promise<void>`
- `isReady()` → `boolean`
- `registerListeners()` → `void`
- `outputChannelLog(...args: unknown[])` → `void`
- `fileLog(...args: unknown[])` → `Promise<void>`
- `setConfiguration(settings: RooCodeSettings)` → `Promise<void>`
- `createProfile(profile: ProviderSettings)` → `Promise<void>`

**Exported Types:**
- `class API`: outputChannel, sidebarProvider, context, taskMap

**Exported Constants:**
- `RooCodeEventName` = `string`
- `TaskCommandName` = `string`
- `isSecretStateKey` = `string`
- `IpcOrigin` = `string`
- `IpcMessageType` = `string`

**Key Imports:** `vscode`, `@roo-code/types`, `@roo-code/ipc`, `events`, `fs/promises`

---

### src\i18n\index.ts
**Purpose:** Provides i18n functionality to initialize, get, change language, and translate strings.

**Exported Functions:**
- `initializeI18n(language: string)` → `void`
- `getCurrentLanguage()` → `string`
- `changeLanguage(language: string)` → `void`
- `t(key: string, options?: Record<string, any>)` → `string`

**Key Imports:** `./setup`

---

### src\i18n\setup.ts
---

### src\integrations\claude-code\__tests__\message-filter.spec.ts
---

### src\integrations\claude-code\__tests__\run.spec.ts
**Functions:** `createMockProcess`, `await`, `next`

---

### src\integrations\claude-code\message-filter.ts
**Purpose:** Filters image blocks from messages for Claude Code compatibility by replacing them with placeholders.

**Exported Functions:**
- `filterMessagesForClaudeCode(messages: Anthropic.Messages.MessageParam[])` → `Anthropic.Messages.MessageParam[]`

**Key Imports:** `@anthropic-ai/sdk`

---

### src\integrations\claude-code\run.ts
**Purpose:** Runs Claude Code process, parses output, and handles errors for code execution.

**Exported Functions:**
- `runClaudeCode(options: ClaudeCodeOptions & { maxOutputTokens?: number })` → `AsyncGenerator<ClaudeCodeMessage | string>`

**Key Imports:** `vscode`, `execa`, `readline`, `os`, `@roo-code/types`

---

### src\integrations\claude-code\types.ts
---

### src\integrations\diagnostics\__tests__\diagnostics.spec.ts
---

### src\integrations\diagnostics\index.ts
**Purpose:** Compares old and new diagnostics to find new problems.

**Exported Functions:**
- `getNewDiagnostics(oldDiagnostics: [vscode.Uri, vscode.Diagnostic[]][], newDiagnostics: [vscode.Uri, vscode.Diagnostic[]][]): [vscode.Uri, vscode.Diagnostic[]][]` → `[vscode.Uri, vscode.Diagnostic[]][]`

**Key Imports:** `vscode`, `path`, `fast-deep-equal`

---

### src\integrations\editor\__tests__\detect-omission.spec.ts
**Functions:** `example`, `generateLongContent`

---

### src\integrations\editor\__tests__\DiffViewProvider.spec.ts
**Functions:** `label`, `tab`, `view`

---

### src\integrations\editor\__tests__\EditorUtils.spec.ts
**Functions:** `constructor`

---

### src\integrations\editor\DecorationController.ts
**Purpose:** Manages text editor decorations for highlighting lines.

**Exported Types:**
- `type DecorationType`

**Key Imports:** `vscode`

---

### src\integrations\editor\detect-omission.ts
**Purpose:** Detects potential AI-generated code omissions in file content.

**Exported Functions:**
- `detectCodeOmission(originalFileContent: string, newFileContent: string, predictedLineCount: number): boolean` → `boolean`

**Key Imports:** `vscode`

---

### src\integrations\editor\DiffViewProvider.ts
**Purpose:** Provides a diff view for comparing file changes.

**Exported Types:**
- `class DiffViewProvider`: newProblemsMessage, userEdits, editType, isEditing, originalContent

**Exported Constants:**
- `DIFF_VIEW_URI_SCHEME` = `"cline-diff"`
- `DIFF_VIEW_LABEL_CHANGES` = `"Original ↔ Roo's Changes"`

**Key Imports:** `vscode`, `path`, `fs/promises`, `diff`, `strip-bom`

---

### src\integrations\editor\EditorUtils.ts
**Purpose:** Utility functions for interacting with the VSCode editor.

**Exported Types:**
- `interface EffectiveRange`: range, text
- `interface DiagnosticData`: message, severity, code, source, range
- `interface EditorContext`: filePath, selectedText, startLine, endLine, diagnostics

**Key Imports:** `vscode`, `path`

---

### src\integrations\misc\__tests__\extract-text-from-xlsx.test.ts
---

### src\integrations\misc\__tests__\extract-text-large-files.spec.ts
**Functions:** `example`, `mockResolvedValue`, `toContain`

---

### src\integrations\misc\__tests__\extract-text.spec.ts
---

### src\integrations\misc\__tests__\line-counter.spec.ts
**Functions:** `mockImplementation`

---

### src\integrations\misc\__tests__\open-file.spec.ts
---

### src\integrations\misc\__tests__\performance\processCarriageReturns.benchmark.ts
**Functions:** `random`, `generateTestData`, `generateLongLineTestData`, `generateHighDensityCRData`, `getIterationCount`, `calculateStats`, `runPerformanceTest`, `runBaselineTest`, `runBenchmark`

---

### src\integrations\misc\__tests__\read-file-tool.spec.ts
**Functions:** `test`, `mockReturnValue`

---

### src\integrations\misc\__tests__\read-lines.spec.ts
**Functions:** `withTempFile`

---

### src\integrations\misc\export-markdown.ts
**Purpose:** Exports conversation history as a Markdown file.

**Exported Functions:**
- `downloadTask(dateTs: number, conversationHistory: Anthropic.MessageParam[])` → `Promise<void>`
- `formatContentBlockToMarkdown(block: any)` → `string`
- `findToolName(tool_code: string)` → `string`

**Key Imports:** `@anthropic-ai/sdk`, `os`, `path`, `vscode`

---

### src\integrations\misc\extract-text-from-xlsx.ts
**Purpose:** Extracts text content from XLSX files.

**Exported Functions:**
- `extractTextFromXLSX(filePathOrWorkbook: string | ExcelJS.Workbook): Promise<string>` → `Promise<string>`

**Key Imports:** `exceljs`

---

### src\integrations\misc\extract-text.ts
**Purpose:** Extracts text from various file formats like PDF, DOCX, XLSX, IPYNB.

**Exported Functions:**
- `getSupportedBinaryFormats()` → `Record<string, (filePath: string) => Promise<string>>`
- `extractTextFromFile(filePath: string): Promise<string>` → `Promise<string>`

**Key Imports:** `path`, `pdf-parse/lib/pdf-parse`, `mammoth`, `fs/promises`

---

### src\integrations\misc\image-handler.ts
**Purpose:** Handles opening and saving image files.

**Exported Functions:**
- `openImage(dataUriOrPath: string, options?: { values?: { action?: string } })` → `Promise<void>`
- `saveImage(imageUri: vscode.Uri, options?: { values?: { action?: string } })` → `Promise<void>`

**Key Imports:** `path`, `os`, `vscode`, `../../utils/path`, `../../i18n`

---

### src\integrations\misc\line-counter.ts
**Purpose:** Counts the number of lines in a file efficiently.

**Exported Functions:**
- `countFileLines(filePath: string): Promise<number>` → `Promise<number>`

**Key Imports:** `fs`, `readline`

---

### src\integrations\misc\open-file.ts
**Purpose:** Opens a file path, attempting decoding and resolving relative paths.

**Exported Functions:**
- `openFile(filePath: string, options: OpenFileOptions = {})` → `Promise<void>`

**Exported Types:**
- `interface OpenFileOptions`: create?: boolean, content?: string, line?: number

**Key Imports:** `path`, `os`, `vscode`, `../../utils/path`, `../../i18n`

---

### src\integrations\misc\process-images.ts
**Purpose:** Selects images via dialog and converts them to base64 data URLs.

**Exported Functions:**
- `selectImages()` → `Promise<string[]>`

**Key Imports:** `vscode`, `fs/promises`, `path`

---

### src\integrations\misc\read-lines.ts
**Purpose:** Reads a specified range of lines from a file asynchronously.

**Exported Functions:**
- `readLines(filepath: string, endLine?: number, startLine?: number)` → `Promise<string>`

**Key Imports:** `fs`

---

### src\integrations\terminal\__tests__\ExecaTerminal.spec.ts
---

### src\integrations\terminal\__tests__\ExecaTerminalProcess.spec.ts
---

### src\integrations\terminal\__tests__\setupTerminalTests.ts
**Functions:** `isPowerShellCoreAvailable`

---

### src\integrations\terminal\__tests__\streamUtils\bashStream.ts
**Functions:** `createBashCommandStream`

---

### src\integrations\terminal\__tests__\streamUtils\cmdStream.ts
**Functions:** `createCmdCommandStream`

---

### src\integrations\terminal\__tests__\streamUtils\index.ts
**Functions:** `isPowerShellCoreAvailable`, `getPlatform`, `isWindows`

---

### src\integrations\terminal\__tests__\streamUtils\mockStream.ts
**Functions:** `createBaseMockStream`, `createBashMockStream`, `createCmdMockStream`, `createPowerShellMockStream`, `createChunkedMockStream`

---

### src\integrations\terminal\__tests__\streamUtils\pwshStream.ts
**Functions:** `createPowerShellStream`

---

### src\integrations\terminal\__tests__\TerminalProcess.spec.ts
---

### src\integrations\terminal\__tests__\TerminalProcessExec.bash.spec.ts
**Functions:** `createRealCommandStream`, `testTerminalCommand`, `constructor`

---

### src\integrations\terminal\__tests__\TerminalProcessExec.cmd.spec.ts
**Functions:** `testCmdCommand`, `onLine`, `constructor`

---

### src\integrations\terminal\__tests__\TerminalProcessExec.common.ts
**Purpose:** Defines common test categories and parameters for terminal process execution tests.

**Exported Constants:**
- `TEST_PURPOSES` = `{ BASIC_OUTPUT: string, OUTPUT_WITHOUT_NEWLINE: string, MULTILINE_OUTPUT: string, EXIT_CODE_SUCCESS: string, EXIT_CODE_ERROR: string, ... }`
- `LARGE_OUTPUT_PARAMS` = `{ LINES: 10 }`
- `TEST_TEXT` = `{ BASIC: "a", MULTILINE_FIRST: "a", MULTILINE_SECOND: "b", LARGE_PREFIX: "Line " }`

---

### src\integrations\terminal\__tests__\TerminalProcessExec.pwsh.spec.ts
**Functions:** `testPowerShellCommand`, `onLine`, `constructor`, `foreach`

---

### src\integrations\terminal\__tests__\TerminalProcessInterpretExitCode.spec.ts
---

### src\integrations\terminal\__tests__\TerminalRegistry.spec.ts
---

### src\integrations\terminal\BaseTerminal.ts
**Purpose:** Abstract base class managing common terminal state and output processing.

**Exported Functions:**
- `setActiveStream(stream: AsyncIterable<string> | undefined, pid?: number)` → `void`

**Exported Types:**
- `class BaseTerminal`: provider: RooTerminalProvider, id: number, initialCwd: string, busy: boolean, running: boolean

**Key Imports:** `../misc/extract-text`, `@roo-code/types`, `./types`

---

### src\integrations\terminal\BaseTerminalProcess.ts
**Purpose:** Abstract base class for terminal processes emitting events upon completion.

**Exported Types:**
- `class BaseTerminalProcess`: command: string, isHot: boolean, fullOutput: string, lastRetrievedIndex: number

**Key Imports:** `events`, `./types`

---

### src\integrations\terminal\ExecaTerminal.ts
**Purpose:** Implements a terminal using the execa library for command execution.

**Exported Types:**
- `class ExecaTerminal`: provider: RooTerminalProvider, id: number, initialCwd: string, busy: boolean, running: boolean

**Key Imports:** `./types`, `./BaseTerminal`, `./ExecaTerminalProcess`, `./mergePromise`

---

### src\integrations\terminal\ExecaTerminalProcess.ts
**Purpose:** Manages an external process execution using execa.

**Exported Types:**
- `class ExecaTerminalProcess`: command: string, isHot: boolean, fullOutput: string, lastRetrievedIndex: number

**Key Imports:** `execa`, `ps-tree`, `process`, `./types`, `./BaseTerminalProcess`

---

### src\integrations\terminal\mergePromise.ts
**Functions:** `mergePromise`, `nativePromisePrototype`

---

### src\integrations\terminal\ShellIntegrationManager.ts
**Functions:** `clear`

---

### src\integrations\terminal\Terminal.ts
**Functions:** `constructor`

---

### src\integrations\terminal\TerminalProcess.ts
**Functions:** `constructor`, `run`, `await`, `continue`, `abort`, `emitRemainingBufferIfListening`

---

### src\integrations\terminal\TerminalRegistry.ts
**Functions:** `initialize`, `cleanup`, `removeTerminal`

---

### src\integrations\terminal\types.ts
---

### src\integrations\theme\getTheme.ts
**Purpose:** Retrieves the active VS Code color theme configuration for use in the application.

**Exported Functions:**
- `getTheme()` → `Promise<any>`

**Exported Types:**
- `type defaultThemes`: Default Dark Modern: string, Dark+: string, Dark (Visual Studio): string, Dark High Contrast: string, Light+: string

**Key Imports:** `vscode`, `path`, `fs/promises`, `monaco-vscode-textmate-theme-converter/lib/cjs`, `../../shared/package`

---

### src\integrations\workspace\__tests__\WorkspaceTracker.spec.ts
---

### src\integrations\workspace\WorkspaceTracker.ts
**Purpose:** Tracks workspace files and open tabs, notifying the provider of changes.

**Exported Types:**
- `class WorkspaceTracker`: cwd: string, constructor(provider: ClineProvider), initializeFilePaths(): Promise<void>, dispose(): void

**Key Imports:** `vscode`, `path`, `../../services/glob/list-files`, `../../core/webview/ClineProvider`, `../../utils/path`

---

### src\services\browser\__tests__\BrowserSession.spec.ts
---

### src\services\browser\__tests__\UrlContentFetcher.spec.ts
---

### src\services\browser\browserDiscovery.ts
**Purpose:** Provides utilities for discovering and checking connectivity to Chrome browser instances.

**Exported Functions:**
- `isPortOpen(host: string, port: number, timeout?: number)` → `Promise<boolean>`
- `tryChromeHostUrl(chromeHostUrl: string)` → `Promise<boolean>`
- `getDockerHostIP()` → `Promise<string | null>`

**Key Imports:** `net`, `axios`, `dns`

---

### src\services\browser\BrowserSession.ts
**Purpose:** Manages a persistent Puppeteer browser session for web interactions and screenshots.

**Exported Types:**
- `class BrowserSession`: context: vscode.ExtensionContext, browser?: Browser, page?: Page, constructor(context: vscode.ExtensionContext), waitTillHTMLStable(): Promise<void>
- `interface PCRStats`: puppeteer: { launch: typeof launch }, executablePath: string

**Key Imports:** `vscode`, `fs/promises`, `path`, `puppeteer-core`, `p-wait-for`

---

### src\services\browser\UrlContentFetcher.ts
**Purpose:** Fetches and converts content from a given URL into markdown format.

**Exported Types:**
- `class UrlContentFetcher`: context: vscode.ExtensionContext, browser?: Browser, page?: Page, constructor(context: vscode.ExtensionContext)
- `interface PCRStats`: puppeteer: { launch: typeof launch }, executablePath: string

**Key Imports:** `vscode`, `fs/promises`, `path`, `puppeteer-core`, `cheerio`

---

### src\services\checkpoints\__tests__\excludes.spec.ts
---

### src\services\checkpoints\__tests__\ShadowCheckpointService.spec.ts
**Functions:** `initWorkspaceRepo`

---

### src\services\checkpoints\excludes.ts
**Functions:** `getBuildArtifactPatterns`, `getMediaFilePatterns`, `getCacheFilePatterns`, `getConfigFilePatterns`, `getLargeDataFilePatterns`, `getDatabaseFilePatterns`, `getGeospatialPatterns`, `getLogFilePatterns`, `getLfsPatterns`, `getExcludePatterns`

---

### src\services\checkpoints\index.ts
---

### src\services\checkpoints\RepoPerTaskCheckpointService.ts
**Functions:** `create`

---

### src\services\checkpoints\ShadowCheckpointService.ts
**Functions:** `baseHash`, `isInitialized`, `writeExcludeFile`, `stageAll`, `getShadowGitConfigWorktree`, `restoreCheckpoint`, `hashWorkspaceDir`, `taskRepoDir`, `workspaceRepoDir`, `deleteTask`, `deleteBranch`

---

### src\services\checkpoints\types.ts
---

### src\services\code-index\__tests__\cache-manager.spec.ts
---

### src\services\code-index\__tests__\config-manager.spec.ts
**Functions:** `setupSecretMocks`

---

### src\services\code-index\__tests__\manager.spec.ts
---

### src\services\code-index\__tests__\service-factory.spec.ts
---

### src\services\code-index\cache-manager.ts
**Functions:** `constructor`

---

### src\services\code-index\config-manager.ts
**Functions:** `constructor`

---

### src\services\code-index\constants\index.ts
---

### src\services\code-index\embedders\__tests__\gemini.spec.ts
**Purpose:** Tests GeminiEmbedder's instantiation and model configuration.

**Key Imports:** `vitest`, `type { MockedClass } from "vitest"`, `GeminiEmbedder`, `OpenAICompatibleEmbedder`, `@roo-code/telemetry`

---

### src\services\code-index\embedders\__tests__\mistral.spec.ts
**Purpose:** Tests MistralEmbedder's instantiation and API key handling.

**Key Imports:** `type { MockedClass } from "vitest"`, `MistralEmbedder`, `OpenAICompatibleEmbedder`, `@roo-code/telemetry`

---

### src\services\code-index\embedders\__tests__\ollama.spec.ts
**Purpose:** Tests the Ollama embedder's interaction with the Ollama service.

**Key Imports:** `type { MockedFunction } from "vitest"`, `CodeIndexOllamaEmbedder`, `@roo-code/telemetry`

---

### src\services\code-index\embedders\__tests__\openai-compatible-rate-limit.spec.ts
**Purpose:** Tests OpenAICompatibleEmbedder's rate limiting and retry mechanisms.

**Key Imports:** `type { MockedClass, MockedFunction } from "vitest"`, `OpenAI`, `OpenAICompatibleEmbedder`, `@roo-code/telemetry`

---

### src\services\code-index\embedders\__tests__\openai-compatible.spec.ts
**Purpose:** Tests OpenAICompatibleEmbedder's embedding creation and error handling.

**Exported Functions:**
- `createMockResponse` → ``
- `createBase64Embedding` → ``
- `expectEmbeddingValues` → ``

**Key Imports:** `type { MockedClass, MockedFunction } from "vitest"`, `OpenAI`, `OpenAICompatibleEmbedder`, `MAX_ITEM_TOKENS`, `INITIAL_RETRY_DELAY_MS`, `@roo-code/telemetry`

---

### src\services\code-index\embedders\__tests__\openai.spec.ts
**Purpose:** Tests OpenAiEmbedder's embedding creation and error handling.

**Key Imports:** `type { MockedClass, MockedFunction } from "vitest"`, `OpenAI`, `OpenAiEmbedder`, `MAX_ITEM_TOKENS`, `INITIAL_RETRY_DELAY_MS`, `@roo-code/telemetry`

---

### src\services\code-index\embedders\__tests__\vercel-ai-gateway.spec.ts
**Purpose:** Tests VercelAiGatewayEmbedder's instantiation and model configuration.

**Key Imports:** `VercelAiGatewayEmbedder`, `OpenAICompatibleEmbedder`, `@roo-code/telemetry`

---

### src\services\code-index\embedders\gemini.ts
**Functions:** `constructor`

---

### src\services\code-index\embedders\mistral.ts
**Functions:** `constructor`

---

### src\services\code-index\embedders\ollama.ts
**Functions:** `constructor`

---

### src\services\code-index\embedders\openai-compatible.ts
**Functions:** `constructor`

---

### src\services\code-index\embedders\openai.ts
**Functions:** `constructor`

---

### src\services\code-index\embedders\vercel-ai-gateway.ts
**Functions:** `constructor`

---

### src\services\code-index\interfaces\cache.ts
**Purpose:** Defines the interface for a code index cache manager.

**Exported Types:**
- `interface ICacheManager`: getHash(filePath: string): string | undefined, updateHash(filePath: string, hash: string): void, deleteHash(filePath: string): void, getAllHashes(): Record<string, string>

---

### src\services\code-index\interfaces\config.ts
**Purpose:** Defines configuration interfaces for the code indexing feature.

**Exported Types:**
- `interface CodeIndexConfig`: isConfigured: boolean, embedderProvider: EmbedderProvider, modelId?: string, modelDimension?: number, openAiOptions?: ApiHandlerOptions
- `type PreviousConfigSnapshot`: enabled: boolean, configured: boolean, embedderProvider: EmbedderProvider, modelId?: string, modelDimension?: number

**Key Imports:** `ApiHandlerOptions`, `EmbedderProvider`

---

### src\services\code-index\interfaces\embedder.ts
**Purpose:** Defines interfaces for code index embedders and their responses.

**Exported Types:**
- `interface IEmbedder`: createEmbeddings(texts: string[], model?: string): Promise<EmbeddingResponse>, validateConfiguration(): Promise<{ valid: boolean; error?: string }>, get embedderInfo(): EmbedderInfo
- `interface EmbeddingResponse`: embeddings: number[][], usage?: { promptTokens: number; totalTokens: number }
- `type AvailableEmbedders`
- `interface EmbedderInfo`: name: AvailableEmbedders

---

### src\services\code-index\interfaces\file-processor.ts
**Purpose:** Defines interfaces for file parsing, directory scanning, and watching.

**Exported Types:**
- `interface ICodeParser`: parseFile(filePath: string, options?: { minBlockLines?: number; maxBlockLines?: number; content?: string; fileHash?: string }): Promise<CodeBlock[]>
- `interface IDirectoryScanner`: scanDirectory(directory: string, onError?: (error: Error) => void, onBlocksIndexed?: (indexedCount: number) => void, onFileParsed?: (fileBlockCount: number) => void): Promise<{ stats: { processed: number; skipped: number }; totalBlockCount: number }>
- `interface IFileWatcher`: initialize(): Promise<void>, readonly onDidStartBatchProcessing: vscode.Event<string[], readonly onDidFinishBatchProcessing: vscode.Event<BatchProcessingSummary>, dispose(): void

**Key Imports:** `vscode`, `PointStruct`

---

### src\services\code-index\interfaces\index.ts
**Purpose:** Exports all interfaces related to code indexing.

**Key Imports:** `embedder`, `vector-store`, `file-processor`, `manager`

---

### src\services\code-index\interfaces\manager.ts
**Purpose:** Defines the interface for the code index manager.

**Exported Types:**
- `interface ICodeIndexManager`: onProgressUpdate: vscode.Event<{ systemStatus: IndexingState; fileStatuses: Record<string, string>; message?: string }>, readonly state: IndexingState, readonly isFeatureEnabled: boolean, readonly isFeatureConfigured: boolean, loadConfiguration(): Promise<void>

**Key Imports:** `VectorStoreSearchResult`, `vscode`

---

### src\services\code-index\interfaces\vector-store.ts
**Purpose:** Defines interfaces for vector database clients and data structures.

**Exported Types:**
- `type PointStruct`: id: string, vector: number[], payload: Record<string, any>
- `interface IVectorStore`: initialize(): Promise<boolean>, upsertPoints(points: PointStruct[]): Promise<void>, search(queryVector: number[], directoryPrefix?: string, minScore?: number, maxResults?: number): Promise<VectorStoreSearchResult[]>

---

### src\services\code-index\manager.ts
**Purpose:** Manages the code indexing process, including configuration and state.

**Exported Functions:**
- `CodeIndexManager` → ``
- `getCurrentStatus` → ``

**Key Imports:** `vscode`, `VectorStoreSearchResult`, `IndexingState`, `CodeIndexConfigManager`, `CodeIndexStateManager`, `CodeIndexServiceFactory`, `CodeIndexSearchService`, `CodeIndexOrchestrator`, `CacheManager`, `RooIgnoreController`, `fs`, `ignore`, `path`, `t`, `TelemetryService`, `TelemetryEventName`

---

### src\services\code-index\orchestrator.ts
**Purpose:** Orchestrates the code indexing workflow using various services and managers.

**Exported Functions:**
- `CodeIndexOrchestratorconfigManager: CodeIndexConfigManager, stateManager: CodeIndexStateManager, workspacePath: string, cacheManager: CacheManager, vectorStore: IVectorStore, scanner: DirectoryScanner, fileWatcher: IFileWatcher` → ``

**Key Imports:** `vscode`, `path`, `CodeIndexConfigManager`, `CodeIndexStateManager`, `IFileWatcher`, `IVectorStore`, `BatchProcessingSummary`, `DirectoryScanner`, `CacheManager`, `TelemetryService`, `TelemetryEventName`, `t`

---

### src\services\code-index\processors\__tests__\file-watcher.spec.ts
---

### src\services\code-index\processors\__tests__\parser.spec.ts
**Functions:** `test`, `calculate`, `processItems`, `sum`, `f`, `g`, `mockCapture`, `constructor`, `add`

---

### src\services\code-index\processors\__tests__\parser.vb.spec.ts
---

### src\services\code-index\processors\__tests__\scanner.spec.ts
**Functions:** `main`

---

### src\services\code-index\processors\file-watcher.ts
**Purpose:** Implements a file watcher to track changes and trigger indexing.

**Exported Functions:**
- `FileWatcher` → ``

**Exported Constants:**
- `MAX_FILE_SIZE_BYTES` = `number`
- `BATCH_SEGMENT_THRESHOLD` = `number`
- `MAX_BATCH_RETRIES` = `number`
- `INITIAL_RETRY_DELAY_MS` = `number`

**Key Imports:** `vscode`, `QDRANT_CODE_BLOCK_NAMESPACE`, `MAX_FILE_SIZE_BYTES`, `BATCH_SEGMENT_THRESHOLD`, `MAX_BATCH_RETRIES`, `INITIAL_RETRY_DELAY_MS`, `createHash`, `RooIgnoreController`, `uuidv5`, `Ignore`, `scannerExtensions`, `IFileWatcher`, `FileProcessingResult`, `IEmbedder`, `IVectorStore`, `PointStruct`, `BatchProcessingSummary`, `codeParser`, `CacheManager`, `generateNormalizedAbsolutePath`, `generateRelativeFilePath`, `isPathInIgnoredDirectory`, `TelemetryService`, `TelemetryEventName`, `sanitizeErrorMessage`, `Package`

---

### src\services\code-index\processors\index.ts
**Purpose:** This file exports modules for parsing, scanning, and watching files.

---

### src\services\code-index\processors\parser.ts
**Purpose:** This file parses code files into code blocks for indexing.

**Exported Functions:**
- `finalizeChunk` → `void`
- `createSegmentBlock` → `void`

**Exported Types:**
- `class CodeParser`: loadedParsers, pendingLoads

**Key Imports:** `fs/promises`, `crypto`, `path`, `web-tree-sitter`, `@roo-code/telemetry`

---

### src\services\code-index\processors\scanner.ts
**Purpose:** This file scans directories for code files and processes them.

**Exported Types:**
- `class DirectoryScanner`: batchSegmentThreshold, parsingConcurrency

**Key Imports:** `../../glob/list-files`, `ignore`, `../../../core/ignore/RooIgnoreController`, `fs/promises`, `path`

---

### src\services\code-index\search-service.ts
**Purpose:** This file searches the code index for relevant content.

**Exported Types:**
- `class CodeIndexSearchService`

**Key Imports:** `path`, `./interfaces`, `./interfaces/embedder`, `./interfaces/vector-store`, `./config-manager`

---

### src\services\code-index\service-factory.ts
**Purpose:** This file creates and configures code indexing service dependencies.

**Exported Types:**
- `class CodeIndexServiceFactory`: configManager, workspacePath, cacheManager

**Key Imports:** `vscode`, `./embedders/openai`, `./embedders/ollama`, `./embedders/openai-compatible`, `./embedders/gemini`

---

### src\services\code-index\shared\__tests__\get-relative-path.spec.ts
---

### src\services\code-index\shared\__tests__\validation-helpers.spec.ts
---

### src\services\code-index\shared\get-relative-path.ts
**Purpose:** This file generates normalized absolute and relative file paths.

**Exported Functions:**
- `generateNormalizedAbsolutePathfilePath: string, workspaceRoot: string` → `string`
- `generateRelativeFilePathnormalizedAbsolutePath: string, workspaceRoot: string` → `string`

**Key Imports:** `path`

---

### src\services\code-index\shared\supported-extensions.ts
**Purpose:** This file defines supported extensions and fallback chunking rules.

**Exported Functions:**
- `shouldUseFallbackChunkingextension: string` → `boolean`

**Key Imports:** `../../tree-sitter`

---

### src\services\code-index\shared\validation-helpers.ts
**Purpose:** This file sanitizes error messages by removing sensitive information.

**Exported Functions:**
- `sanitizeErrorMessageerrorMessage: string` → `string`

**Key Imports:** `../../../i18n`, `serialize-error`

---

### src\services\code-index\state-manager.ts
**Purpose:** This file manages the state of the code index.

**Exported Types:**
- `type IndexingState`
- `class CodeIndexStateManager`: state, onProgressUpdate

**Key Imports:** `vscode`

---

### src\services\code-index\vector-store\__tests__\qdrant-client.spec.ts
**Functions:** `helper`, `Button`, `InputField`

---

### src\services\code-index\vector-store\qdrant-client.ts
**Functions:** `constructor`

---

### src\services\command\__tests__\built-in-commands.spec.ts
---

### src\services\command\__tests__\frontmatter-commands.spec.ts
---

### src\services\command\built-in-commands.ts
**Functions:** `getBuiltInCommands`, `getBuiltInCommand`, `getBuiltInCommandNames`

---

### src\services\command\commands.ts
**Functions:** `getCommands`, `getCommand`, `tryLoadCommand`, `getCommandNames`, `scanCommandDirectory`, `getCommandNameFromFile`, `isMarkdownFile`

---

### src\services\glob\__mocks__\list-files.ts
---

### src\services\glob\__tests__\gitignore-integration.spec.ts
---

### src\services\glob\__tests__\gitignore-test.spec.ts
**Purpose:** Tests gitignore support within the listFiles function.

**Key Imports:** `path`, `fs`, `os`, `../../ripgrep`, `../../path`

---

### src\services\glob\__tests__\list-files-limit.spec.ts
**Purpose:** Tests stack overflow prevention when listing files with limits.

**Exported Functions:**
- `createMockDirEntry(name: string)` → `any`

**Key Imports:** `path`, `fs`, `../list-files`, `../../ripgrep`, `../../../utils/path`

---

### src\services\glob\__tests__\list-files.spec.ts
**Purpose:** Tests listFiles functionality including edge cases and mocks.

**Exported Functions:**
- `mockResolvedValueOnce()` → `any`

**Key Imports:** `path`, `child_process`, `../list-files`, `../../ripgrep`, `../list-files`

---

### src\services\glob\constants.ts
---

### src\services\glob\ignore-utils.ts
**Functions:** `isPathInIgnoredDirectory`

---

### src\services\glob\list-files.ts
**Functions:** `listFiles`, `getFirstLevelDirectories`, `ensureFirstLevelDirectoriesIncluded`, `handleSpecialDirectories`, `getRipgrepPath`, `listFilesWithRipgrep`, `buildRipgrepArgs`, `buildRecursiveArgs`, `buildNonRecursiveArgs`, `createIgnoreInstance`, `findGitignoreFiles`, `listFilteredDirectories`, `scanDirectory`, `matchesIgnorePattern`, `isIgnoredByGitignore`, `shouldIncludeTargetDirectory`, `shouldIncludeInsideHiddenTarget`, `shouldIncludeRegularDirectory`, `shouldIncludeDirectory`, `isDirectoryExplicitlyIgnored`, `formatAndCombineResults`, `execRipgrep`, `processRipgrepOutput`

---

### src\services\marketplace\__tests__\marketplace-setting-check.spec.ts
**Purpose:** Tests marketplace API call authorization based on feature flags.

**Key Imports:** `../../../core/webview/webviewMessageHandler`

---

### src\services\marketplace\__tests__\MarketplaceManager.spec.ts
**Purpose:** Unit tests for the MarketplaceManager class functionality.

**Key Imports:** `@roo-code/types`, `../MarketplaceManager`, `@roo-code/cloud`, `axios`, `../../../../packages/telemetry/src/TelemetryService`, `vscode`

---

### src\services\marketplace\__tests__\nested-parameters.spec.ts
**Purpose:** Validates Zod schemas for MCP installation methods with nested parameters.

**Key Imports:** `@roo-code/types`, `@roo-code/types`

---

### src\services\marketplace\__tests__\optional-parameters.spec.ts
**Purpose:** Validates Zod schema for MCP parameters, focusing on optional fields.

**Key Imports:** `@roo-code/types`

---

### src\services\marketplace\__tests__\RemoteConfigLoader.spec.ts
**Purpose:** Tests fetching and caching marketplace configuration from the remote API.

**Key Imports:** `axios`, `../RemoteConfigLoader`, `@roo-code/types`, `@roo-code/cloud`

---

### src\services\marketplace\__tests__\SimpleInstaller.spec.ts
**Purpose:** Tests the installation logic provided by the SimpleInstaller class.

**Key Imports:** `../SimpleInstaller`, `fs/promises`, `yaml`, `vscode`, `os`, `@roo-code/types`, `../../../core/config/CustomModesManager`, `path`, `../../../utils/fs`

---

### src\services\marketplace\index.ts
**Purpose:** Exports primary components and types from the marketplace service.

**Exported Types:**
- `type MarketplaceItemType`

**Key Imports:** `./SimpleInstaller`, `./MarketplaceManager`, `@roo-code/types`

---

### src\services\marketplace\MarketplaceManager.ts
**Purpose:** Manages fetching and presenting marketplace items to the user.

**Exported Functions:**
- `constructor(context: vscode.ExtensionContext, customModesManager?: CustomModesManager)` → `void`

**Exported Types:**
- `interface MarketplaceItemsResponse`: organizationMcps, marketplaceItems, errors

**Key Imports:** `fs/promises`, `path`, `vscode`, `yaml`, `@roo-code/types`, `@roo-code/telemetry`, `@roo-code/cloud`, `../../shared/globalFileNames`, `../../utils/globalContext`, `../../i18n`, `../../core/config/CustomModesManager`, `./RemoteConfigLoader`, `./SimpleInstaller`

---

### src\services\marketplace\RemoteConfigLoader.ts
**Purpose:** Loads marketplace configuration data from remote API endpoints.

**Exported Types:**
- `type MarketplaceItem`
- `type MarketplaceItemType`

**Key Imports:** `axios`, `yaml`, `z`, `@roo-code/types`, `@roo-code/cloud`

---

### src\services\marketplace\SimpleInstaller.ts
**Purpose:** Handles installation logic for marketplace mode and MCP items.

**Exported Types:**
- `interface InstallOptions`: target, selectedIndex

**Key Imports:** `vscode`, `path`, `fs/promises`, `yaml`, `@roo-code/types`, `../../shared/globalFileNames`, `../../utils/globalContext`, `../../core/config/CustomModesManager`

---

### src\services\mcp\__tests__\McpHub.spec.ts
---

### src\services\mcp\McpHub.ts
**Purpose:** Manages connections and file watching for Model Context Protocol servers.

**Exported Functions:**
- `createServerTypeSchema()` → `z.ZodType<any>`
- `setupFileWatcher(server: McpServer)` → `Promise<void>`
- `removeAllFileWatchers()` → `void`
- `removeFileWatchersForServer(server: McpServer)` → `void`

**Exported Types:**
- `type ConnectedMcpConnection`: type, server, client, transport

**Key Imports:** `@modelcontextprotocol/sdk/client/index.js`, `@modelcontextprotocol/sdk/client/stdio.js`, `@modelcontextprotocol/sdk/client/sse.js`, `@modelcontextprotocol/sdk/client/streamableHttp.js`, `reconnecting-eventsource`, `@modelcontextprotocol/sdk/types.js`, `chokidar`, `delay`, `fast-deep-equal`, `fs/promises`, `path`, `vscode`, `z`, `../../i18n`, `../../core/webview/ClineProvider`, `../../shared/globalFileNames`, `../../shared/mcp`, `../../utils/fs`, `../../utils/path`, `../../utils/config`

---

### src\services\mcp\McpServerManager.ts
**Purpose:** Provides singleton access and lifecycle management for the McpHub instance.

**Key Imports:** `vscode`, `./McpHub`, `../../core/webview/ClineProvider`

---

### src\services\mdm\__tests__\MdmService.spec.ts
---

### src\services\mdm\MdmService.ts
---

### src\services\ripgrep\__tests__\index.spec.ts
---

### src\services\ripgrep\index.ts
**Functions:** `processData`, `truncateLine`, `getBinPath`, `execRipgrep`, `regexSearchFiles`, `formatResults`, `checkPath`

---

### src\services\roo-config\__tests__\index.spec.ts
---

### src\services\roo-config\index.ts
**Functions:** `getGlobalRooDirectory`, `getProjectRooDirectoryForCwd`, `directoryExists`, `fileExists`, `readFileIfExists`, `getRooDirectoriesForCwd`, `loadConfiguration`

---

### src\services\search\file-search.ts
**Functions:** `executeRipgrep`, `executeRipgrepForFiles`, `searchWorkspaceFiles`

---

### src\services\tree-sitter\__tests__\fixtures\sample-c-sharp.ts
**Functions:** `TestAttributeDefinition`, `TestClassDefinition`, `TestInterfaceMethod`, `TestInterfaceCalculateMethod`, `TestEventArgsDefinition`, `TestStructDefinition`, `ToString`, `TestRecordDefinition`, `TestRecordMethodDefinition`, `TestPartialMethod1`, `TestPartialMethod2`, `TestExtensionMethod1`, `TestExtensionMethod2`, `new`, `TestGenericClassMethod1`, `TestGenericClassMethod2`, `TestOuterClassDefinition`, `TestNestedMethod`, `TestAsyncMethodDefinition`, `TestAsyncPrivateMethod1`, `TestAsyncPrivateMethod2`, `TestDerivedClass1`, `TestDerivedClass2`, `TestFileScopedMethod`, `TestLinqMethod`

---

### src\services\tree-sitter\__tests__\fixtures\sample-c.ts
**Functions:** `basic_multitype_function`, `array_param_function`, `pointer_param_function`, `variadic_impl_function`, `test_variadic_function`

---

### src\services\tree-sitter\__tests__\fixtures\sample-cpp.ts
**Functions:** `function_with_implementation`, `destructor_test`

---

### src\services\tree-sitter\__tests__\fixtures\sample-css.ts
**Functions:** `and`

---

### src\services\tree-sitter\__tests__\fixtures\sample-elisp.ts
---

### src\services\tree-sitter\__tests__\fixtures\sample-elixir.ts
---

### src\services\tree-sitter\__tests__\fixtures\sample-embedded_template.ts
---

### src\services\tree-sitter\__tests__\fixtures\sample-go.ts
**Functions:** `TestChannelDefinition`, `TestGoroutineDefinition`, `func`, `TestDeferDefinition`, `TestSelectDefinition`

---

### src\services\tree-sitter\__tests__\fixtures\sample-html.ts
**Purpose:** Demonstrates HTML structure with various elements and attributes.

**Exported Functions:**
- `testFunction` → ``

---

### src\services\tree-sitter\__tests__\fixtures\sample-java.ts
**Purpose:** Illustrates Java syntax including interfaces, enums, and classes.

**Exported Functions:**
- `testInterfaceDefaultMethodString input, T data` → `String`
- `formatMessageString message, Object... args` → `String`

**Exported Types:**
- `interface TestInterfaceDefinition`: testInterfaceMethod(String message, T data), testInterfaceDefaultMethod(String input, T data)
- `enum TestEnumDefinition`: DEBUG(0, "Debug Level"), INFO(1, "Info Level"), WARNING(2, "Warning Level"), ERROR(3, "Error Level")
- `class TestClassDefinition`: String message, T data
- `class TestAbstractClassDefinition`: abstractMethod(), concreteMethod()
- `class TestInnerClassDefinition`: innerMethod()
- `class TestStaticNestedClassDefinition`: staticNestedMethod()
- `class TestRecordDefinition`: String message, T data

**Key Imports:** `java.util.List`, `java.util.Map`, `java.util.function.Function`, `java.time.LocalDateTime`

---

### src\services\tree-sitter\__tests__\fixtures\sample-javascript.ts
**Purpose:** Demonstrates JavaScript syntax including functions and classes.

**Exported Functions:**
- `testFunctionDefinitionparam1, param2, param3` → ``
- `testAsyncFunctionDefinitionurl, options, timeout` → ``
- `testGeneratorFunctionDefinitionstart, end, step` → ``
- `testArrowFunctionDefinitionparam1, param2, callback` → ``
- `testMethodDefinitionparam1, param2` → ``
- `testStaticMethodDefinitionparam1, param2` → ``
- `testGetterDefinition` → ``
- `testSetterDefinitionvalue` → ``
- `testDecoratedMethodDefinitionparam1, param2` → ``

**Exported Types:**
- `class TestClassDefinition`: #privateField, static staticField, constructor(name, value), testMethodDefinition(param1, param2)

**Key Imports:** `react`, `react-dom`, `./utils`

---

### src\services\tree-sitter\__tests__\fixtures\sample-json.ts
**Purpose:** Provides a sample JSON structure with various data types.

---

### src\services\tree-sitter\__tests__\fixtures\sample-kotlin.ts
**Purpose:** Illustrates Kotlin syntax including classes, interfaces, and enums.

**Exported Functions:**
- `concreteMethodDefinitionparam1: String, param2: Int` → `Int`
- `requiredMethodDefinitionparam1: String, param2: Int` → `Boolean`
- `defaultMethodDefinitionmessage: String = "default"` → `String`

**Exported Types:**
- `class TestAbstractClassDefinition`: abstractPropertyDefinition: String, abstractMethodDefinition(): String, concreteMethodDefinition(param1: String, param2: Int)
- `interface TestInterfaceDefinition`: interfacePropertyDefinition: String, requiredMethodDefinition(param1: String, param2: Int), defaultMethodDefinition(message: String = "default")
- `enum TestEnumClassDefinition`: enumValue: Int, enumDescription: String
- `class TestOuterClassDefinition`: TestInnerClassDefinition
- `class TestInnerClassDefinition`: innerMethod()
- `class TestNestedClassDefinition`: nestedMethod()
- `class TestSealedClassDefinition`: sealedMethod()

**Key Imports:** `kotlinx.coroutines.*`, `kotlinx.coroutines.flow.*`, `kotlin.math.sqrt`, `kotlin.properties.Delegates`

---

### src\services\tree-sitter\__tests__\fixtures\sample-lua.ts
**Purpose:** Demonstrates Lua syntax including functions and tables.

**Exported Functions:**
- `test_functionarg1, arg2, arg3` → ``
- `test_local_functionparam1, param2, param3` → ``

---

### src\services\tree-sitter\__tests__\fixtures\sample-ocaml.ts
**Purpose:** Shows OCaml syntax with modules, types, and functions.

**Exported Types:**
- `type StringSet`: type t, val empty: t, val add: string -> t -> t, val mem: string -> t -> bool
- `type shape`: Rectangle of float * float, Circle of float, Triangle of float * float * float
- `type person`: name: string, age: int, address: string option, phone: string list

---

### src\services\tree-sitter\__tests__\fixtures\sample-php.ts
**Purpose:** Demonstrates PHP syntax including classes, traits, and attributes.

**Exported Functions:**
- `standardMethodDefinition` → ``
- `standardInterfaceMethodWithClass` → ``
- `standardInterfaceMethodNullable` → ``
- `standardInterfaceMethodVoid` → ``
- `standardInterfaceMethodMixed` → ``
- `standardTraitMethod` → ``
- `standardTraitAbstractMethod` → ``
- `standardEnumMethod` → ``
- `standardEnumFromString` → ``
- `standardAbstractMethod` → ``
- `standardStaticMethod` → ``
- `validateConfig` → ``
- `standardUnionTypesMethod` → ``
- `standardIntersectionTypesMethod` → ``
- `standardAnonymousMethod` → ``
- `standardGlobalFunction` → ``
- `match` → ``

**Exported Types:**
- `class StandardAttributeDefinition`: private string $description, private int $priority, private array $tags
- `class StandardClassDefinition`: private string $standardProperty, public function standardMethod(): string

**Key Imports:** `StandardNamespaceDefinition\Interfaces\StandardInterfaceDefinition`, `StandardNamespaceDefinition\Interfaces\AnotherInterfaceDefinition`, `StandardNamespaceDefinition\Traits\StandardTraitDefinition`, `StandardNamespaceDefinition\Traits\LoggableTraitDefinition`, `StandardNamespaceDefinition\Enums\StandardEnumDefinition`, `StandardNamespaceDefinition\Attributes\StandardAttributeDefinition`

---

### src\services\tree-sitter\__tests__\fixtures\sample-python.ts
**Purpose:** Illustrates Python syntax with classes, functions, and decorators.

---

### src\services\tree-sitter\__tests__\fixtures\sample-ruby.ts
**Purpose:** Shows Ruby syntax with classes and method definitions.

---

### src\services\tree-sitter\__tests__\fixtures\sample-rust.ts
**Purpose:** Demonstrates Rust syntax including functions and structs.

**Exported Functions:**
- `test_function_definitionparam1: i32, param2: &str, param3: Option<String>, param4: Vec<u8>` → `Result<i32, String>`
- `test_async_function_definitionurl: &str, timeout: std::time::Duration, retry_count: u32, headers: Vec<(&str, &str)>` → `Result<String, Box<dyn std::error::Error>>`
- `test_const_function_definitionvalue: T, multiplier: usize, prefix: &'static str, suffix: &'static str` → `[T; 4]`
- `is_nullvalue: &Option<T>` → `bool`

**Exported Types:**
- `class test_struct_definition`: name: String, value: i32, data: Option<Vec<f64>>, metadata: std::collections::HashMap<String, i32>
- `class test_tuple_struct_definition`: String, i32, Option<Vec<f64>>, std::collections::HashMap<String, i32>

---

### src\services\tree-sitter\__tests__\fixtures\sample-scala.ts
**Purpose:** Illustrates Scala syntax including classes, traits, and objects.

**Exported Functions:**
- `RichStringval str: String` → ``

**Exported Types:**
- `class Container`: val first: A, val second: B, swap: Container[B, A]
- `class TestCaseClass`: field1: A, field2: B, field3: List[A]
- `class AbstractBase`: abstractMethod: String, abstractValue: Int
- `type TestTrait`: type T, method[A](param1: A, param2: List[T]): Option[A]
- `class PatternMatcher`: testMatch(value: Any): Int

**Key Imports:** `scala.collection.mutable`, `scala.concurrent.Future`

---

### src\services\tree-sitter\__tests__\fixtures\sample-solidity.ts
**Purpose:** Demonstrates Solidity syntax with interfaces, libraries, and contracts.

**Exported Functions:**
- `interfaceFunctionuint256 value` → `bool`
- `adduint256 a, uint256 b` → `uint256`
- `subtractuint256 a, uint256 b` → `uint256`
- `transferaddress to, uint256 amount` → ``
- `returns` → ``
- `onlyAdmin` → ``
- `constructoruint256 _totalSupply` → ``

**Exported Types:**
- `interface ITestInterface`: interfaceFunction(uint256 value), event InterfaceEvent(address indexed sender, uint256 value), error InterfaceError(string message)
- `class UserInfo`: address userAddress, uint256 balance, mapping(bytes32 => bool) permissions, uint256 lastUpdate
- `enum UserRole`: None, Basic, Admin, SuperAdmin

---

### src\services\tree-sitter\__tests__\fixtures\sample-swift.ts
**Purpose:** Illustrates Swift syntax including classes, structs, and methods.

**Exported Functions:**
- `standardMethod` → `String`
- `finalClassMethodparameter: String` → `Int`
- `openOverridableMethodparameter1: String, parameter2: Int` → `Double`
- `protocolRequiredMethodwith parameter: String` → `Bool`
- `standardStructMethod` → `String`
- `mutatingMethod` → ``
- `initparameter: String` → ``

**Exported Types:**
- `class StandardClassDefinition`: private var standardProperty: String, standardMethod()
- `class FinalClassDefinition`: private let finalProperty: Int, finalClassMethod(parameter: String)
- `class OpenClassDefinition`: public var openProperty: Double, openOverridableMethod(parameter1: String, parameter2: Int)
- `class InheritingClassDefinition`: protocolRequiredProperty: String, override func standardMethod(), func protocolRequiredMethod(with parameter: String)
- `class StandardStructDefinition`: private var standardStructProperty: String, let readOnlyProperty: Int, mutatingMethod()

---

### src\services\tree-sitter\__tests__\fixtures\sample-systemrdl.ts
**Purpose:** Defines a sample SystemRDL code snippet for testing tree-sitter parsing.

---

### src\services\tree-sitter\__tests__\fixtures\sample-tlaplus.ts
**Purpose:** Defines a sample TLA+ module with operators, functions, and procedures for testing.

---

### src\services\tree-sitter\__tests__\fixtures\sample-toml.ts
**Purpose:** Defines a sample TOML configuration file with various data structures.

**Exported Constants:**
- `sampleToml` = ``# This is a TOML document with various structures`

---

### src\services\tree-sitter\__tests__\fixtures\sample-tsx.ts
**Purpose:** Defines sample TSX content with React components and TypeScript types for testing.

**Exported Types:**
- `interface StandardInterfaceProps`: required, numeric, callback, complex
- `type StandardTypeAlias`: id, name, timestamp, status
- `interface PropsDefinitionExample`: requiredString, requiredNumber, requiredCallback, optionalBoolean

---

### src\services\tree-sitter\__tests__\fixtures\sample-typescript.ts
**Purpose:** Defines sample TypeScript code with interfaces, types, enums, and functions for testing.

**Exported Types:**
- `interface TestInterfaceDefinition`: name, value, methodSignature
- `type TestTypeDefinition`: id, name, callback
- `enum TestEnumDefinition`: First, Second, Third, Fourth

**Key Imports:** `react`, `react-dom`

---

### src\services\tree-sitter\__tests__\fixtures\sample-vue.ts
**Purpose:** Defines a sample Vue component with template, script, props, methods, and computed properties.

**Exported Constants:**
- `sampleVue` = ``
<template>
  <div class="example-component">
    <h1>{{ title }}</h1>
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </nav>
    <slot name="content"></slot>
  </div>
</template>

<script>
export default {
  name: 'ExampleComponent',
  
  components: {
    ChildComponent,
    AnotherComponent,
    ThirdComponent,
    FourthComponent
  },

  props: {
    title: {
      type: String,
      required: true,
      default: 'Default Title',
      validator: function(value) {
        return value.length > 0
      }
    }
  },

  methods: {
    handleSubmit(event) {
      this.validateForm();
      this.processData();
      this.$emit('submit', this.formData);
      this.resetForm();
    }
  },

  computed: {
    fullName: {
      get() {
        return `\${this.firstName} \${this.lastName}`;
      },
      set(value) {
        [this.firstName, this.lastName] = value.split(' ');
        this.$emit('update:fullName', value);
      }
    }
  },

  watch: {
    searchQuery: {
      handler(newVal, oldVal) {
        this.debouncedSearch();
        this.updateHistory();
        this.logChange(newVal, oldVal);
        this.updateUI();
      },
      immediate: true,
      deep: true
    }
  },

  beforeCreate() {
    this.loadInitialState();
    this.setupEventListeners();
    this.initializePlugins();
    this.validateConfigurat`

---

### src\services\tree-sitter\__tests__\fixtures\sample-zig.ts
**Purpose:** Defines a sample Zig code snippet with structs, functions, enums, and variables.

**Exported Types:**
- `type Point`: x, y, init, distance
- `type Vector`: direction, magnitude

---

### src\services\tree-sitter\__tests__\helpers.ts
**Purpose:** Provides helper functions for initializing tree-sitter and testing source code parsing.

**Exported Functions:**
- `initializeTreeSitter()` → `Promise<{ Parser: typeof Parser; Language: typeof Language }>`
- `testParseSourceCodeDefinitionsfilename: string, sourceCode: string, options: any` → `Promise<string | null>`
- `inspectTreeStructuresourceCode: string, language: string` → `Promise<string>`
- `debugLogmessage: string, ...args: any[]` → `void`

**Exported Constants:**
- `DEBUG` = `process.env.DEBUG ? parseInt(process.env.DEBUG, 10) : 0`

**Key Imports:** `fs/promises`, `path`, `../queries/tsx`, `web-tree-sitter`

---

### src\services\tree-sitter\__tests__\index.spec.ts
**Functions:** `test`, `CheckboxExample`, `mockResolvedValue`, `constructor`, `testMethod`, `function`

---

### src\services\tree-sitter\__tests__\inspectC.spec.ts
---

### src\services\tree-sitter\__tests__\inspectCpp.spec.ts
---

### src\services\tree-sitter\__tests__\inspectCSharp.spec.ts
---

### src\services\tree-sitter\__tests__\inspectCSS.spec.ts
---

### src\services\tree-sitter\__tests__\inspectElisp.spec.ts
---

### src\services\tree-sitter\__tests__\inspectElixir.spec.ts
---

### src\services\tree-sitter\__tests__\inspectEmbeddedTemplate.spec.ts
---

### src\services\tree-sitter\__tests__\inspectGo.spec.ts
---

### src\services\tree-sitter\__tests__\inspectHtml.spec.ts
---

### src\services\tree-sitter\__tests__\inspectJava.spec.ts
---

### src\services\tree-sitter\__tests__\inspectJavaScript.spec.ts
**Purpose:** Tests the inspection of JavaScript code structure and definitions.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectJson.spec.ts
**Purpose:** Tests the inspection of JSON code structure and definitions.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectKotlin.spec.ts
**Purpose:** Tests the inspection of Kotlin code structure and definitions.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectLua.spec.ts
**Purpose:** Tests the inspection of Lua code structure and definitions.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectOCaml.spec.ts
**Purpose:** Tests the inspection of OCaml code structure and definitions.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectPhp.spec.ts
**Purpose:** Tests the inspection of PHP code structure and definitions.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectPython.spec.ts
**Purpose:** Tests Python code inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectRuby.spec.ts
**Purpose:** Tests the inspection of Ruby code structure and definitions.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectRust.spec.ts
**Purpose:** Tests Rust code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectScala.spec.ts
**Purpose:** Tests Scala code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectSolidity.spec.ts
**Purpose:** Tests Solidity code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectSwift.spec.ts
**Purpose:** Tests Swift code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectSystemRDL.spec.ts
**Purpose:** Tests SystemRDL code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectTLAPlus.spec.ts
**Purpose:** Tests TLA+ code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectTOML.spec.ts
**Purpose:** Tests TOML code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectTsx.spec.ts
**Purpose:** Tests TSX code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectTypeScript.spec.ts
**Purpose:** Tests TypeScript code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectVue.spec.ts
**Purpose:** Tests Vue code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\inspectZig.spec.ts
**Purpose:** Tests Zig code structure inspection and definition parsing.

**Key Imports:** `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\languageParser.spec.ts
**Purpose:** Tests loading language parsers based on file extensions.

**Key Imports:** `path`, `vitest`, `vitest/dist/reporters-5f08277e`, `vitest/dist/index-27940049`, `vitest/dist/index-27940049`

---

### src\services\tree-sitter\__tests__\markdownIntegration.spec.ts
**Purpose:** Tests markdown integration for parsing source code definitions.

**Exported Functions:**
- `parseSourceCodeDefinitionsForFile` → `Promise<void>`

**Key Imports:** `fs/promises`, `vitest`, `../index`, `../../../utils/fs`

---

### src\services\tree-sitter\__tests__\markdownParser.spec.ts
**Purpose:** Tests parsing markdown content and formatting captures.

**Exported Functions:**
- `parseMarkdown` → `any`

**Key Imports:** `../markdownParser`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.c-sharp.spec.ts
**Purpose:** Tests C# source code definition parsing using tree-sitter.

**Key Imports:** `fs/promises`, `../languageParser`, `../../../utils/fs`, `../queries`, `./helpers`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.c.spec.ts
**Purpose:** Tests C source code definition parsing capabilities.

**Key Imports:** `./helpers`, `../queries`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.cpp.spec.ts
**Purpose:** Tests C++ source code definition parsing via tree-sitter.

**Key Imports:** `./helpers`, `../queries`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.css.spec.ts
**Purpose:** Tests CSS source code definition parsing functionality.

**Key Imports:** `./helpers`, `../queries`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.elisp.spec.ts
**Purpose:** Tests Elisp source code definition parsing.

**Key Imports:** `./helpers`, `../queries/elisp`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.elixir.spec.ts
**Purpose:** Tests Elixir source code definition parsing.

**Key Imports:** `../queries`, `./helpers`, `fs/promises`, `../languageParser`, `../../../utils/fs`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.embedded_template.spec.ts
**Purpose:** Tests embedded template source code definition parsing.

**Key Imports:** `./helpers`, `../queries`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.go.spec.ts
**Purpose:** Tests Go source code definition parsing.

**Key Imports:** `./fixtures/sample-go`, `./helpers`, `../queries/go`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.html.spec.ts
**Purpose:** Tests HTML source code definition parsing.

**Key Imports:** `./fixtures/sample-html`, `../queries`, `./helpers`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.java.spec.ts
**Purpose:** Tests Java source code definition parsing.

**Key Imports:** `../queries`, `./helpers`, `./fixtures/sample-java`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.javascript.spec.ts
**Purpose:** Tests JavaScript source code definition parsing.

**Key Imports:** `./helpers`, `../queries`, `./fixtures/sample-javascript`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.json.spec.ts
**Purpose:** Tests JSON structure parsing using JavaScript tree-sitter.

**Key Imports:** `./helpers`, `../queries`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.kotlin.spec.ts
**Purpose:** Tests Kotlin source code definition parsing.

**Key Imports:** `../queries`, `./helpers`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.lua.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.ocaml.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.php.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.python.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.ruby.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.rust.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.scala.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.solidity.spec.ts
**Functions:** `toMatch`

---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.swift.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.systemrdl.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.tlaplus.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.toml.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.tsx.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.typescript.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.vue.spec.ts
---

### src\services\tree-sitter\__tests__\parseSourceCodeDefinitions.zig.spec.ts
---

### src\services\tree-sitter\index.ts
**Functions:** `getMinComponentLines`, `setMinComponentLines`, `parseSourceCodeDefinitionsForFile`, `parseSourceCodeForDefinitionsTopLevel`, `separateFiles`, `processCaptures`, `parseFile`

---

### src\services\tree-sitter\languageParser.ts
**Functions:** `loadLanguage`, `loadRequiredLanguageParsers`

---

### src\services\tree-sitter\markdownParser.ts
**Functions:** `parseMarkdown`, `formatMarkdownCaptures`

---

### src\services\tree-sitter\queries\c-sharp.ts
---

### src\services\tree-sitter\queries\c.ts
**Functions:** `definitions`, `declarations`

---

### src\services\tree-sitter\queries\cpp.ts
---

### src\services\tree-sitter\queries\css.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying CSS language constructs.

**Exported Constants:**
- `cssQuery`

---

### src\services\tree-sitter\queries\elisp.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Emacs Lisp definitions.

**Exported Constants:**
- `elispQuery`

---

### src\services\tree-sitter\queries\elixir.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Elixir language definitions.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\embedded_template.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying embedded template structures.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\go.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Go language declarations.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\html.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying HTML document structures and elements.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\index.ts
**Purpose:** Aggregates and re-exports Tree-Sitter query strings for various programming languages.

**Exported Constants:**
- `solidityQuery`
- `phpQuery`
- `vueQuery`
- `typescriptQuery`
- `tsxQuery`
- `pythonQuery`
- `javascriptQuery`
- `javaQuery`
- `rustQuery`
- `rubyQuery`
- `cppQuery`
- `cQuery`
- `csharpQuery`
- `goQuery`
- `swiftQuery`
- `kotlinQuery`
- `cssQuery`
- `elixirQuery`
- `htmlQuery`
- `luaQuery`
- `ocamlQuery`
- `tomlQuery`
- `systemrdlQuery`
- `tlaPlusQuery`
- `zigQuery`
- `embeddedTemplateQuery`
- `elispQuery`
- `scalaQuery`

**Key Imports:** `./solidity`, `./php`, `./vue`, `./typescript`, `./tsx`

---

### src\services\tree-sitter\queries\java.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Java language structures.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\javascript.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying JavaScript definitions and methods.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\kotlin.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Kotlin class and function declarations.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\lua.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Lua function and variable definitions.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\ocaml.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying OCaml module and type definitions.

**Exported Constants:**
- `ocamlQuery`

---

### src\services\tree-sitter\queries\php.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying PHP language constructs.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\python.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Python definitions and statements.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\ruby.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Ruby methods, classes, and modules.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\rust.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Rust functions, structs, and traits.

**Exported Constants:**
- `default`

---

### src\services\tree-sitter\queries\scala.ts
**Purpose:** Defines Tree-Sitter query patterns for identifying Scala classes, objects, and methods.

**Exported Constants:**
- `scalaQuery`

---

### src\services\tree-sitter\queries\solidity.ts
---

### src\services\tree-sitter\queries\swift.ts
---

### src\services\tree-sitter\queries\systemrdl.ts
---

### src\services\tree-sitter\queries\tlaplus.ts
---

### src\services\tree-sitter\queries\toml.ts
---

### src\services\tree-sitter\queries\tsx.ts
---

### src\services\tree-sitter\queries\typescript.ts
---

### src\services\tree-sitter\queries\vue.ts
---

### src\services\tree-sitter\queries\zig.ts
---

### src\shared\__tests__\api.spec.ts
---

### src\shared\__tests__\checkExistApiConfig.spec.ts
---

### src\shared\__tests__\combineApiRequests.spec.ts
---

### src\shared\__tests__\combineCommandSequences.spec.ts
---

### src\shared\__tests__\context-mentions.spec.ts
**Functions:** `hash`, `whitespace`, `logs`, `cases`, `backslash`, `mentions`

---

### src\shared\__tests__\experiments-preventFocusDisruption.spec.ts
---

### src\shared\__tests__\experiments.spec.ts
---

### src\shared\__tests__\getApiMetrics.spec.ts
---

### src\shared\__tests__\language.spec.ts
---

### src\shared\__tests__\modes-empty-prompt-component.spec.ts
---

### src\shared\__tests__\modes.spec.ts
---

### src\shared\__tests__\ProfileValidator.spec.ts
---

### src\shared\__tests__\support-prompts.spec.ts
**Functions:** `test`

---

### src\shared\__tests__\vsCodeSelectorUtils.spec.ts
---

### src\shared\api.ts
**Purpose:** Defines API handler options, router names, and utility functions for provider routing.

**Exported Functions:**
- `isRouterName(value: string)` → `value is RouterName`
- `toRouterName(value?: string)` → `RouterName`

**Exported Types:**
- `type ApiHandlerOptions`: enableGpt5ReasoningSummary?: boolean, ollamaNumCtx?: number
- `type RouterName`
- `type ModelRecord`
- `type RouterModels`

**Key Imports:** `@roo-code/types`

---

### src\shared\array.ts
**Purpose:** Provides utility functions to find the last element or index matching a predicate in an array.

**Exported Functions:**
- `findLastIndex<T>(array: Array<T>, predicate: (value: T, index: number, obj: T[]) => boolean)` → `number`
- `findLast<T>(array: Array<T>, predicate: (value: T, index: number, obj: T[]) => boolean)` → `T | undefined`

---

### src\shared\checkExistApiConfig.ts
**Purpose:** Checks if a given provider configuration contains necessary API keys or settings.

**Exported Functions:**
- `checkExistKey(config: ProviderSettings | undefined)` → `boolean`

**Key Imports:** `@roo-code/types`

---

### src\shared\combineApiRequests.ts
**Purpose:** Combines API request start and finish messages into a single combined message.

**Exported Functions:**
- `combineApiRequests(messages: ClineMessage[])` → `ClineMessage[]`

**Key Imports:** `@roo-code/types`

---

### src\shared\combineCommandSequences.ts
**Purpose:** Merges sequential command and command output messages into unified entries.

**Exported Functions:**
- `combineCommandSequences(messages: ClineMessage[])` → `ClineMessage[]`

**Exported Constants:**
- `COMMAND_OUTPUT_STRING` = `"Output:"`

**Key Imports:** `@roo-code/types`, `./safeJsonParse`

---

### src\shared\context-mentions.ts
**Functions:** `formatGitSuggestion`, `unescapeSpaces`

---

### src\shared\cost.ts
**Purpose:** Calculates API usage costs based on token counts and model pricing information.

**Exported Functions:**
- `calculateApiCostAnthropic(modelInfo: ModelInfo, inputTokens: number, outputTokens: number, cacheCreationInputTokens?: number, cacheReadInputTokens?: number)` → `number`
- `calculateApiCostOpenAI(modelInfo: ModelInfo, inputTokens: number, outputTokens: number, cacheCreationInputTokens?: number, cacheReadInputTokens?: number)` → `number`

**Key Imports:** `@roo-code/types`

---

### src\shared\embeddingModels.ts
**Purpose:** Defines profiles and dimensions for various embedding models used across providers.

**Exported Types:**
- `type EmbedderProvider`
- `interface EmbeddingModelProfile`: dimension: number, scoreThreshold?: number, queryPrefix?: string
- `type EmbeddingModelProfiles`

**Exported Constants:**
- `EMBEDDING_MODEL_PROFILES`

---

### src\shared\experiments.ts
**Purpose:** Manages feature flag configurations and provides utilities for checking experiment status.

**Exported Types:**
- `type ExperimentKey`
- `interface ExperimentConfig`: enabled: boolean

**Exported Constants:**
- `EXPERIMENT_IDS`
- `experimentConfigsMap`
- `experimentDefault`
- `experiments`

**Key Imports:** `@roo-code/types`

---

### src\shared\ExtensionMessage.ts
**Purpose:** Defines interfaces for messages and data structures exchanged between the extension and webview.

**Exported Types:**
- `interface Command`: name: string, source: "global" | "project" | "built-in", filePath?: string, description?: string, argumentHint?: string
- `interface MarketplaceInstalledMetadata`: project: Record<string, { type: string }>, global: Record<string, { type: string }>
- `interface IndexingStatus`: systemStatus: string, message?: string, processedItems: number, totalItems: number, currentItemUnit?: string
- `interface IndexingStatusUpdateMessage`: type: "indexingStatusUpdate", values: IndexingStatus
- `interface LanguageModelChatSelector`: vendor?: string, family?: string, version?: string, id?: string

**Key Imports:** `@roo-code/types`, `../utils/git`, `./mcp`, `./modes`, `./api`

---

### src\shared\getApiMetrics.ts
**Purpose:** Calculates total token usage, cache operations, and cost from an array of Cline messages.

**Exported Functions:**
- `getApiMetrics(messages: ClineMessage[])` → `TokenUsage`

**Exported Types:**
- `type ParsedApiReqStartedTextType`: tokensIn: number, tokensOut: number, cacheWrites: number, cacheReads: number, cost?: number, apiProtocol?: "anthropic" | "openai"

**Key Imports:** `@roo-code/types`

---

### src\shared\globalFileNames.ts
**Purpose:** Defines standardized filenames used for storing global configuration and metadata.

**Exported Constants:**
- `GlobalFileNames` = `{ apiConversationHistory: "api_conversation_history.json", uiMessages: "ui_messages.json", mcpSettings: "mcp_settings.json", customModes: "custom_modes.yaml", taskMetadata: "task_metadata.json" }`

---

### src\shared\language.ts
**Purpose:** Provides language code mapping and formats VSCode locale strings to standard language codes.

**Exported Functions:**
- `formatLanguage(vscodeLocale: string)` → `Language`

**Exported Constants:**
- `LANGUAGES`

**Key Imports:** `@roo-code/types`

---

### src\shared\mcp.ts
**Purpose:** Defines data structures for managing and communicating with the Multi-Cloud Provider server.

**Exported Types:**
- `type McpErrorEntry`: message: string, timestamp: number, level: "error" | "warn" | "info"
- `type McpServer`: name: string, config: string, status: "connected" | "connecting" | "disconnected", error?: string, errorHistory?: McpErrorEntry[]
- `type McpTool`: name: string, description?: string, inputSchema?: object, alwaysAllow?: boolean, enabledForPrompt?: boolean
- `type McpResource`: uri: string, name: string, mimeType?: string, description?: string
- `type McpResourceResponse`: _meta?: Record<string, any>, contents: Array<{ uri: string, mimeType?: string, text?: string, blob?: string }>

---

### src\shared\modes.ts
**Purpose:** Provides utilities for managing and querying configuration details of various operational modes.

**Exported Functions:**
- `getGroupName(group: GroupEntry)` → `ToolGroup`
- `doesFileMatchRegex(filePath: string, pattern: string)` → `boolean`
- `getToolsForMode(groups: readonly GroupEntry[])` → `string[]`

**Exported Types:**
- `type Mode`

**Key Imports:** `vscode`, `@roo-code/types`, `../core/prompts/sections/custom-instructions`, `./experiments`, `./tools`

---

### src\shared\package.ts
**Purpose:** Provides access to core package metadata, potentially overridden by environment variables.

**Exported Constants:**
- `Package`

**Key Imports:** `../package.json`

---

### src\shared\ProfileValidator.ts
---

### src\shared\safeJsonParse.ts
---

### src\shared\support-prompt.ts
**Functions:** `generateDiagnosticText`

---

### src\shared\todo.ts
**Functions:** `getLatestTodo`

---

### src\shared\tools.ts
---

### src\shared\utils\__tests__\requesty.spec.ts
---

### src\shared\utils\requesty.ts
---

### src\shared\vsCodeSelectorUtils.ts
**Functions:** `stringifyVsCodeLmModelSelector`

---

### src\shared\WebviewMessage.ts
---

### src\utils\__tests__\autoImportSettings.spec.ts
---

### src\utils\__tests__\config.spec.ts
---

### src\utils\__tests__\cost.spec.ts
---

### src\utils\__tests__\enhance-prompt.spec.ts
---

### src\utils\__tests__\git.spec.ts
**Functions:** `workspaceFolders`

---

### src\utils\__tests__\migrateSettings.spec.ts
---

### src\utils\__tests__\object.spec.ts
---

### src\utils\__tests__\outputChannelLogger.spec.ts
---

### src\utils\__tests__\path.spec.ts
---

### src\utils\__tests__\safeWriteJson.test.ts
**Functions:** `readFileContent`, `fileExists`

---

### src\utils\__tests__\shell.spec.ts
**Functions:** `mockVsCodeConfig`

---

### src\utils\__tests__\storage.spec.ts
---

### src\utils\__tests__\text-normalization.spec.ts
---

### src\utils\__tests__\tiktoken.spec.ts
---

### src\utils\__tests__\xml-matcher.spec.ts
**Purpose:** Tests XML matching logic for streaming XML parsing.

**Exported Functions:**
- `describe(name: string, fn: () => void)` → `void`
- `it(name: string, fn: () => Promise<void> | void)` → `void`

**Key Imports:** `../xml-matcher`

---

### src\utils\__tests__\xml.spec.ts
**Purpose:** Tests XML parsing functionality, focusing on type preservation.

**Exported Functions:**
- `describe(name: string, fn: () => void)` → `void`
- `it(name: string, fn: () => void)` → `void`

**Key Imports:** `../xml`

---

### src\utils\autoImportSettings.ts
**Purpose:** Automatically imports settings from a specified path during extension activation.

**Exported Functions:**
- `autoImportSettingsoutputChannel: vscode.OutputChannel, { providerSettingsManager, contextProxy, customModesManager }: ImportOptions` → `Promise<void>`
- `resolvePathsettingsPath: string` → `string`

**Key Imports:** `vscode`, `path`, `os`, `../shared/package`, `../i18n`

---

### src\utils\commands.ts
**Purpose:** Provides utility functions for generating command identifiers.

**Exported Functions:**
- `getCommandid: CommandId` → `string`
- `getCodeActionCommandid: CodeActionId` → `string`
- `getTerminalCommandid: TerminalActionId` → `string`

**Exported Constants:**
- `getCommand` = ``${Package.name}.${id}``
- `getCodeActionCommand` = ``${Package.name}.${id}``
- `getTerminalCommand` = ``${Package.name}.${id}``

**Key Imports:** `type { CommandId, CodeActionId, TerminalActionId }`, `../shared/package`

---

### src\utils\config.ts
**Purpose:** Injects environment variables into configuration objects recursively.

**Exported Types:**
- `type InjectableConfigType`: string, [key: string]: undefined | null | boolean | number | InjectableConfigType | Array<undefined | null | boolean | number | InjectableConfigType>

---

### src\utils\countTokens.ts
**Purpose:** Counts tokens in Anthropic messages using worker pool or tiktoken.

**Exported Types:**
- `type CountTokensOptions`: useWorker?: boolean

**Key Imports:** `Anthropic`, `workerpool`, `../workers/types`, `./tiktoken`

---

### src\utils\errors.ts
**Purpose:** Defines a custom error class for organization allowlist violations.

**Exported Types:**
- `class OrganizationAllowListViolationError`: constructor(message: string)

---

### src\utils\focusPanel.ts
**Purpose:** Focuses the active panel, either tab or sidebar, in VS Code.

**Exported Functions:**
- `focusPaneltabPanel: vscode.WebviewPanel | undefined, sidebarPanel: vscode.WebviewView | undefined` → `Promise<void>`

**Key Imports:** `vscode`, `../shared/package`, `../core/webview/ClineProvider`

---

### src\utils\fs.ts
**Purpose:** Provides asynchronous functions for file system operations.

**Exported Functions:**
- `createDirectoriesForFilefilePath: string` → `Promise<string[]>`
- `fileExistsAtPathfilePath: string` → `Promise<boolean>`

**Key Imports:** `fs`, `path`

---

### src\utils\git.ts
**Purpose:** Extracts and provides Git repository information and commit details.

**Exported Types:**
- `interface GitRepositoryInfo`: repositoryUrl?: string, repositoryName?: string, defaultBranch?: string
- `interface GitCommit`: hash: string, shortHash: string, subject: string, author: string, date: string

**Key Imports:** `vscode`, `path`, `fs`, `child_process`, `util`

---

### src\utils\globalContext.ts
**Purpose:** Provides utility functions for accessing global storage paths.

**Exported Functions:**
- `getGlobalFsPathcontext: ExtensionContext` → `Promise<string>`
- `ensureSettingsDirectoryExistscontext: ExtensionContext` → `Promise<string>`

**Key Imports:** `mkdir`, `join`, `vscode`

---

### src\utils\logging\__tests__\CompactLogger.spec.ts
**Purpose:** Tests CompactLogger class, verifying log levels and metadata handling.

**Key Imports:** `../CompactLogger`, `./MockTransport`, `../types`

---

### src\utils\logging\__tests__\CompactTransport.spec.ts
**Purpose:** Tests CompactTransport, ensuring file creation and log writing.

**Exported Functions:**
- `cleanupTestLogs()` → `void`
- `rmDirRecursive(dirPath: string)` → `void`

**Key Imports:** `../CompactTransport`, `fs`, `path`

---

### src\utils\logging\__tests__\MockTransport.ts
**Purpose:** Defines MockTransport for testing logging functionality.

**Exported Types:**
- `class MockTransport`: entries, closed

**Key Imports:** `../CompactTransport`, `../types`

---

### src\utils\logging\CompactLogger.ts
**Purpose:** Implements a compact logger with efficient logging capabilities.

**Exported Types:**
- `class CompactLogger`: transport: CompactTransport, parentMeta: LogMeta | undefined, debug(message: string, meta?: LogMeta): void, info(message: string, meta?: LogMeta): void, warn(message: string, meta?: LogMeta): void

**Key Imports:** `ILogger`, `LogMeta`, `CompactLogEntry`, `LogLevel`, `CompactTransport`

---

### src\utils\logging\CompactTransport.ts
**Purpose:** Implements a compact logging transport with file output support.

**Exported Types:**
- `class CompactTransport`: sessionStart: number, lastTimestamp: number, filePath?: string, initialized: boolean = false, config: CompactTransportConfig = DEFAULT_CONFIG

**Key Imports:** `writeFileSync`, `mkdirSync`, `dirname`, `CompactTransportConfig`, `ICompactTransport`, `CompactLogEntry`, `LogLevel`, `LOG_LEVELS`

---

### src\utils\logging\index.ts
**Purpose:** Provides a default logger instance with Jest environment detection.

**Exported Constants:**
- `logger` = `process.env.NODE_ENV === "test" ? new CompactLogger() : noopLogger`

**Key Imports:** `CompactLogger`

---

### src\utils\logging\types.ts
**Purpose:** Defines core type definitions for the compact logging system.

**Exported Types:**
- `interface CompactLogEntry`: t: number, l: string, m: string, c?: string, d?: unknown
- `type LogLevel`
- `interface LogMeta`: ctx?: string, [key: string]: unknown
- `interface CompactTransportConfig`: level?: LogLevel, fileOutput?: { enabled: boolean, path: string }
- `interface ICompactTransport`: write(entry: CompactLogEntry): void

---

### src\utils\migrateSettings.ts
**Purpose:** Migrates legacy settings files to new locations and formats.

**Exported Functions:**
- `migrateSettings(context: vscode.ExtensionContext, outputChannel: vscode.OutputChannel)` → `Promise<void>`

**Key Imports:** `vscode`, `path`, `fs/promises`, `./fs`, `../shared/globalFileNames`, `yaml`

---

### src\utils\object.ts
**Purpose:** Checks if an object is empty, handling arrays and objects.

**Exported Functions:**
- `isEmpty(obj: unknown)` → `boolean`

---

### src\utils\outputChannelLogger.ts
**Purpose:** Creates logging functions for VSCode output channel and console.

**Exported Types:**
- `type LogFunction`

**Key Imports:** `vscode`

---

### src\utils\path.ts
**Purpose:** Provides path manipulation utilities for consistent path handling.

**Key Imports:** `path`, `os`, `vscode`

---

### src\utils\pathUtils.ts
**Purpose:** Determines if a file path is outside the workspace folders.

**Exported Functions:**
- `isPathOutsideWorkspace(filePath: string)` → `boolean`

**Key Imports:** `vscode`, `path`

---

### src\utils\safeWriteJson.ts
**Purpose:** Safely writes JSON data to a file with locking and backups.

**Exported Functions:**
- `safeWriteJson(filePath: string, data: any)` → `Promise<void>`

**Key Imports:** `fs/promises`, `fs`, `path`, `proper-lockfile`, `stream-json/Disassembler`, `stream-json/Stringer`

---

### src\utils\shell.ts
**Purpose:** Provides utilities for determining the user's shell environment.

**Exported Functions:**
- `getShell()` → `string`

**Key Imports:** `vscode`, `os`, `path`

---

### src\utils\single-completion-handler.ts
**Purpose:** Enhances a prompt using the configured API for completion.

**Exported Functions:**
- `singleCompletionHandler(apiConfiguration: ProviderSettings, promptText: string)` → `Promise<string>`

**Key Imports:** `@roo-code/types`, `../api`

---

### src\utils\storage.ts
**Purpose:** Manages storage paths for conversations and settings, handling custom paths.

**Exported Functions:**
- `getStorageBasePath(defaultPath: string)` → `Promise<string>`
- `getTaskDirectoryPath(storagePath: string, taskId: string)` → `string`
- `getSettingsDirectoryPath(storagePath: string)` → `string`
- `getCacheDirectoryPath(storagePath: string)` → `string`
- `promptForCustomStoragePath()` → `Promise<string | undefined>`

**Key Imports:** `vscode`, `path`, `fs/promises`, `fs`, `../shared/package`, `../i18n`

---

### src\utils\text-normalization.ts
**Purpose:** Normalizes strings by replacing smart quotes and typographic characters.

**Exported Types:**
- `interface NormalizeOptions`: smartQuotes, typographicChars, extraWhitespace, trim

**Exported Constants:**
- `NORMALIZATION_MAPS` = `{}`

---

### src\utils\tiktoken.ts
**Purpose:** Calculates token count for Anthropic messages using tiktoken encoder.

**Exported Functions:**
- `tiktoken(content: Anthropic.Messages.ContentBlockParam[])` → `Promise<number>`

**Key Imports:** `@anthropic-ai/sdk`, `tiktoken/lite`, `tiktoken/encoders/o200k_base`

---

### src\utils\tts.ts
**Purpose:** Provides text-to-speech functionality with queue management and control.

**Exported Functions:**
- `setTtsEnabled(enabled: boolean)` → `(enabled: boolean) => boolean`
- `setTtsSpeed(newSpeed: number)` → `(newSpeed: number) => number`
- `playTts(message: string, options?: PlayTtsOptions)` → `Promise<void>`
- `stopTts()` → `void`

---

### src\utils\vitest-verbosity.ts
**Purpose:** Resolves verbosity settings for Vitest based on command-line arguments.

**Exported Functions:**
- `resolveVerbosity(argv?: string[], env?: NodeJS.ProcessEnv)` → `{ silent: boolean; reporters: string[]; onConsoleLog: (log: string, type: string) => void | false; }`

---

### src\utils\xml-matcher.ts
**Purpose:** Provides XML matching functionality with state management and transformation.

**Exported Types:**
- `interface XmlMatcherResult`: matched, data
- `class XmlMatcher`: index, chunks, cached, matched

---

### src\utils\xml.ts
**Functions:** `parseXml`, `parseXmlForDiff`

---

### src\vitest.config.ts
**Purpose:** Configures Vitest testing environment settings and path aliases.

**Exported Functions:**
- `resolveVerbosity()` → `{ silent: any, reporters: any, onConsoleLog: any }`

**Key Imports:** `vitest/config`, `./utils/vitest-verbosity`

---

### src\vitest.setup.ts
**Purpose:** Sets up Vitest by disabling network requests globally via nock.

**Exported Functions:**
- `allowNetConnect(host?: string | RegExp)` → `void`

**Key Imports:** `nock`, `./utils/path`

---

### src\workers\countTokens.ts
**Purpose:** Exposes a worker function to count tokens using tiktoken utility.

**Exported Functions:**
- `countTokens(content: Anthropic.Messages.ContentBlockParam[])` → `Promise<CountTokensResult>`

**Key Imports:** `workerpool`, `@anthropic-ai/sdk`, `../utils/tiktoken`, `./types`

---

### src\workers\types.ts
**Purpose:** Defines the Zod schema and TypeScript type for token counting results.

**Exported Types:**
- `type CountTokensResult`: success, count, error

**Key Imports:** `zod`

---

### webview-ui\src\__tests__\App.spec.tsx
**Functions:** `ChatView`, `SettingsView`, `HistoryView`, `McpView`, `ModesView`, `MarketplaceView`, `CloudView`, `tFunction`, `MockedComponent`, `triggerMessage`

---

### webview-ui\src\__tests__\command-autocomplete.spec.ts
---

### webview-ui\src\__tests__\ContextWindowProgress.spec.tsx
**Functions:** `renderComponent`

---

### webview-ui\src\__tests__\ContextWindowProgressLogic.spec.ts
---

### webview-ui\src\__tests__\ErrorBoundary.spec.tsx
**Functions:** `tFunction`, `MockedComponent`, `ErrorThrower`

---

### webview-ui\src\__tests__\SearchableSelect.spec.tsx
---

### webview-ui\src\__tests__\TelemetryClient.spec.ts
---

### webview-ui\src\App.tsx
**Purpose:** Main application component managing views and context providers.

**Exported Functions:**
- `App()` → `JSX.Element`
- `AppWithProviders()` → `JSX.Element`

**Key Imports:** `react`, `react-use`, `@tanstack/react-query`, `@roo/ExtensionMessage`, `./i18n/TranslationContext`, `./components/marketplace/MarketplaceViewStateManager`, `./utils/vscode`, `./utils/TelemetryClient`, `./utils/sourceMapInitializer`, `./context/ExtensionStateContext`, `./components/chat/ChatView`, `./components/history/HistoryView`, `./components/settings/SettingsView`, `./components/welcome/WelcomeView`, `./components/mcp/McpView`, `./components/marketplace/MarketplaceView`, `./components/modes/ModesView`, `./components/human-relay/HumanRelayDialog`, `./components/chat/CheckpointRestoreDialog`, `./components/chat/MessageModificationConfirmationDialog`

---

### webview-ui\src\components\__tests__\ErrorBoundary.spec.tsx
**Functions:** `ErrorThrowingComponent`

---

### webview-ui\src\components\chat\__tests__\ApiConfigSelector.spec.tsx
---

### webview-ui\src\components\chat\__tests__\BatchFilePermission.spec.tsx
**Purpose:** Tests the BatchFilePermission component's rendering and behavior.

**Key Imports:** `react`, `@/utils/test-utils`, `@/i18n/__mocks__/TranslationContext`, `../BatchFilePermission`

---

### webview-ui\src\components\chat\__tests__\ChatRow.run-slash-command.spec.tsx
**Purpose:** Tests ChatRow's slash command execution functionality and rendering.

**Exported Functions:**
- `renderChatRowWithProvidersmessage: any, isExpanded = false` → `any`

**Key Imports:** `react`, `@/utils/test-utils`, `vitest`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\__tests__\ChatTextArea.spec.tsx
**Purpose:** Tests the ChatTextArea component's behavior and UI elements.

**Exported Functions:**
- `getEnhancePromptButton` → `any`
- `getApiConfigDropdown` → `any`

**Key Imports:** `@roo/modes`, `@src/utils/test-utils`, `@src/context/ExtensionStateContext`, `@src/utils/vscode`

---

### webview-ui\src\components\chat\__tests__\ChatView.auto-approve-new.spec.tsx
**Purpose:** Tests ChatView component's auto-approve functionality with new messages.

**Exported Functions:**
- `MockBrowserSessionRow{ messages }: { messages: any[] }` → `any`
- `MockChatRow{ message }: { message: any }` → `any`
- `MockTaskHeader{ task }: { task: any }` → `any`
- `mockPostMessage` → `any`
- `renderChatView` → `any`

**Key Imports:** `@/utils/test-utils`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`, `@src/utils/vscode`

---

### webview-ui\src\components\chat\__tests__\ChatView.auto-approve.spec.tsx
**Purpose:** Tests ChatView component's auto-approve functionality.

**Exported Functions:**
- `MockBrowserSessionRow{ messages }: { messages: any[] }` → `any`
- `MockChatRow{ message }: { message: any }` → `any`
- `MockTaskHeader{ task }: { task: any }` → `any`
- `mockPostMessage` → `any`
- `renderChatView` → `any`

**Key Imports:** `@/utils/test-utils`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`, `@src/utils/vscode`

---

### webview-ui\src\components\chat\__tests__\ChatView.keyboard-fix.spec.tsx
**Purpose:** Tests ChatView component's keyboard interaction and fixes.

**Exported Functions:**
- `MockChatTextArea` → `any`
- `mockPostMessage` → `any`
- `renderChatView` → `any`

**Key Imports:** `react`, `@/utils/test-utils`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\__tests__\ChatView.spec.tsx
**Purpose:** Tests the ChatView component's various functionalities and UI.

**Exported Functions:**
- `MockBrowserSessionRow{ messages }: { messages: ClineMessage[] }` → `any`
- `MockChatRow{ message }: { message: ClineMessage }` → `any`
- `MockAnnouncement` → `any`
- `MockDismissibleUpsell` → `any`
- `MockQueuedMessages` → `any`
- `MockRooTips` → `any`
- `MockRooHero` → `any`
- `MockTelemetryBanner` → `any`
- `MockChatTextArea` → `any`
- `MockVSCodeButton` → `any`
- `MockVSCodeTextField` → `any`
- `MockVSCodeLink` → `any`
- `mockPostMessage` → `any`
- `renderChatView` → `any`

**Exported Types:**
- `interface ClineMessage`: type, say?, ask?, ts, text?
- `interface ExtensionState`: version, clineMessages, taskHistory, shouldShowAnnouncement, allowedCommands

**Key Imports:** `react`, `@/utils/test-utils`, `@tanstack/react-query`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\__tests__\CheckpointRestoreDialog.spec.tsx
**Purpose:** Tests the CheckpointRestoreDialog component's rendering and behavior.

**Key Imports:** `react`, `@/utils/test-utils`, `vitest`

---

### webview-ui\src\components\chat\__tests__\CloudTaskButton.spec.tsx
**Purpose:** Tests the CloudTaskButton component's functionality and UI.

**Key Imports:** `react-i18next`, `@/utils/test-utils`, `qrcode`, `@roo-code/cloud/src/config`, `@/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\__tests__\CommandExecution.spec.tsx
**Purpose:** Tests the CommandExecution component's rendering and behavior.

**Exported Functions:**
- `ExtensionStateWrapper{ children }: { children: React.ReactNode }` → `any`

**Key Imports:** `react`, `@testing-library/react`, `../CommandExecution`, `../../../context/ExtensionStateContext`

---

### webview-ui\src\components\chat\__tests__\CommandPatternSelector.spec.tsx
**Purpose:** Tests the CommandPatternSelector component's rendering and interactions.

**Exported Functions:**
- `TestWrapper{ children }: { children: React.ReactNode }` → `any`

**Key Imports:** `react`, `@testing-library/react`, `../CommandPatternSelector`, `../../../components/ui/tooltip`

---

### webview-ui\src\components\chat\__tests__\FollowUpSuggest.spec.tsx
**Purpose:** Tests the FollowUpSuggest component's rendering and behavior.

**Exported Functions:**
- `renderWithTestProviders` → `any`

**Key Imports:** `react`, `@testing-library/react`, `@radix-ui/react-tooltip`, `../FollowUpSuggest`

---

### webview-ui\src\components\chat\__tests__\IndexingStatusBadge.spec.tsx
**Purpose:** Tests the IndexingStatusBadge component's rendering and functionality.

**Exported Functions:**
- `renderComponent` → `any`

**Key Imports:** `react`, `@/utils/test-utils`, `@src/utils/vscode`, `../IndexingStatusBadge`

---

### webview-ui\src\components\chat\__tests__\ModeSelector.spec.tsx
**Purpose:** Tests the ModeSelector component's rendering and behavior.

**Key Imports:** `@/utils/test-utils`, `@roo-code/types`, `@roo/modes`, `../ModeSelector`

---

### webview-ui\src\components\chat\__tests__\ShareButton.spec.tsx
---

### webview-ui\src\components\chat\__tests__\SlashCommandItemSimple.spec.tsx
---

### webview-ui\src\components\chat\__tests__\TaskActions.spec.tsx
---

### webview-ui\src\components\chat\__tests__\TaskHeader.spec.tsx
**Functions:** `renderTaskHeader`

---

### webview-ui\src\components\chat\Announcement.tsx
**Purpose:** Displays dismissible announcements to the user within a dialog.

**Exported Functions:**
- `Announcement{ hideAnnouncement: () => void }` → `JSX.Element`
- `XLink()` → `JSX.Element`
- `DiscordLink()` → `JSX.Element`
- `RedditLink()` → `JSX.Element`

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `@roo/package`, `@src/i18n/TranslationContext`, `@src/context/ExtensionStateContext`, `@src/utils/vscode`, `@src/components/ui`

---

### webview-ui\src\components\chat\ApiConfigSelector.tsx
**Purpose:** Provides a searchable, pinnable dropdown for selecting API configurations.

**Exported Types:**
- `interface ApiConfigSelectorProps`: value, displayName, disabled, title, onChange, triggerClassName, listApiConfigMeta, pinnedApiConfigs, togglePinnedApiConfig

**Key Imports:** `react`, `fzf`, `@/lib/utils`, `@/components/ui/hooks/useRooPortal`, `@/components/ui`, `@/i18n/TranslationContext`, `@/utils/vscode`, `@/components/ui`, `./IconButton`

---

### webview-ui\src\components\chat\AutoApprovedRequestLimitWarning.tsx
**Purpose:** Displays a warning when auto-approved request or cost limits are reached.

**Exported Functions:**
- `AutoApprovedRequestLimitWarning({ message }: AutoApprovedRequestLimitWarningProps)` → `JSX.Element | null`

**Exported Types:**
- `type AutoApprovedRequestLimitWarningProps`: message: ClineMessage

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `react-i18next`, `@roo-code/types`, `@src/utils/vscode`

---

### webview-ui\src\components\chat\AutoApproveDropdown.tsx
**Purpose:** Provides a dropdown menu to manage auto-approval settings for various actions.

**Exported Functions:**
- `AutoApproveDropdown({ disabled?: boolean, triggerClassName?: string })` → `JSX.Element`

**Exported Types:**
- `interface AutoApproveDropdownProps`: disabled?: boolean, triggerClassName?: string

**Key Imports:** `react`, `lucide-react`, `#/utils/vscode`, `#/lib/utils`, `#/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\BatchDiffApproval.tsx
**Purpose:** Renders a list of file diffs for batch approval with expandable accordions.

**Exported Functions:**
- `BatchDiffApproval({ files?: FileDiff[], ts: number })` → `JSX.Element | null`

**Exported Types:**
- `interface FileDiff`: path: string, changeCount: number, key: string, content: string, diffs?: Array<{ content: string, startLine?: number }>
- `interface BatchDiffApprovalProps`: files: FileDiff[], ts: number

**Key Imports:** `react`, `../common/CodeAccordian`

---

### webview-ui\src\components\chat\BatchFilePermission.tsx
**Purpose:** Displays a list of files requiring permission, allowing user interaction.

**Exported Functions:**
- `BatchFilePermission({ files?: FilePermissionItem[], onPermissionResponse?: (response: { [key: string]: boolean }) => void, ts: number })` → `JSX.Element | null`

**Exported Types:**
- `interface FilePermissionItem`: path: string, lineSnippet?: string, isOutsideWorkspace?: boolean, key: string, content?: string
- `interface BatchFilePermissionProps`: files: FilePermissionItem[], onPermissionResponse?: (response: { [key: string]: boolean }) => void, ts: number

**Key Imports:** `react`, `../common/ToolUseBlock`, `@src/utils/vscode`, `@src/utils/removeLeadingNonAlphanumeric`

---

### webview-ui\src\components\chat\BrowserSessionRow.tsx
**Purpose:** Renders a chat row displaying browser session actions and results.

**Exported Functions:**
- `BrowserSessionRow(props: BrowserSessionRowProps)` → `JSX.Element`

**Exported Types:**
- `interface BrowserSessionRowProps`: messages: ClineMessage[], isExpanded: (messageTs: number) => boolean, onToggleExpand: (messageTs: number) => void, lastModifiedMessage?: ClineMessage, isLast: boolean

**Key Imports:** `react`, `react-use`, `fast-deep-equal`, `react-i18next`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\chat\ChatRow.tsx
**Purpose:** Renders a single chat message row, handling various message types and tools.

**Exported Functions:**
- `ChatRowContent(props: any)` → `JSX.Element`

**Key Imports:** `react`, `react-use`, `react-i18next`, `fast-deep-equal`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\chat\ChatTextArea.tsx
**Purpose:** Provides a dynamic textarea for chat input with mention and command features.

**Exported Functions:**
- `ChatTextArea(props: any, ref: React.Ref<HTMLTextAreaElement>)` → `JSX.Element`

**Exported Constants:**
- `MAX_IMAGES_PER_MESSAGE`

**Key Imports:** `react`, `react-use`, `react-textarea-autosize`, `lucide-react`, `@roo/context-mentions`

---

### webview-ui\src\components\chat\ChatView.tsx
**Purpose:** Manages and displays the main chat interface, including message rendering and interactions.

**Exported Functions:**
- `ChatView(props: any, ref: React.Ref<VirtuosoHandle>)` → `JSX.Element`

**Exported Constants:**
- `MAX_IMAGES_PER_MESSAGE`

**Key Imports:** `react`, `react-use`, `debounce`, `react-virtuoso`, `remove-markdown`

---

### webview-ui\src\components\chat\CheckpointRestoreDialog.tsx
**Purpose:** Presents a dialog for confirming message edits or deletions with checkpoint restore options.

**Exported Functions:**
- `CheckpointRestoreDialog({ open: boolean, onOpenChange: (open: boolean) => void, onConfirm: (restoreCheckpoint: boolean) => void, type: "edit" | "delete", hasCheckpoint: boolean })` → `JSX.Element`

**Exported Types:**
- `interface CheckpointRestoreDialogProps`: open: boolean, onOpenChange: (open: boolean) => void, onConfirm: (restoreCheckpoint: boolean) => void, type: "edit" | "delete", hasCheckpoint: boolean

**Key Imports:** `react`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\chat\checkpoints\__tests__\CheckpointSaved.spec.tsx
**Functions:** `waitForOpenHandler`, `getMenu`, `popoverRoot`, `menuContainer`

---

### webview-ui\src\components\chat\checkpoints\CheckpointMenu.tsx
**Purpose:** Provides a menu for checkpoint-related actions like diffing and restoring.

**Exported Functions:**
- `CheckpointMenu({ ts: number, commitHash: string, currentHash?: string, checkpoint: Checkpoint, open?: boolean, onOpenChange?: (open: boolean) => void })` → `JSX.Element`

**Exported Types:**
- `type CheckpointMenuBaseProps`: ts: number, commitHash: string, currentHash?: string, checkpoint: Checkpoint
- `type CheckpointMenuControlledProps`: open: boolean, onOpenChange: (open: boolean) => void
- `type CheckpointMenuUncontrolledProps`: open?: undefined, onOpenChange?: undefined
- `type CheckpointMenuProps`: ts: number, commitHash: string, currentHash?: string, checkpoint: Checkpoint, open?: boolean, onOpenChange?: (open: boolean) => void

**Key Imports:** `react`, `@radix-ui/react-icons`, `react-i18next`, `#/components/ui`, `#/components/ui/hooks`

---

### webview-ui\src\components\chat\checkpoints\CheckpointSaved.tsx
**Purpose:** Displays a saved checkpoint with an interactive menu for further actions.

**Exported Functions:**
- `CheckpointSaved({ checkpoint?: Record<string, unknown>, ts: number, commitHash: string, currentHash?: string })` → `JSX.Element`

**Exported Types:**
- `type CheckpointSavedProps`: ts: number, commitHash: string, currentHash?: string, checkpoint?: Record<string, unknown>

**Key Imports:** `react`, `react-i18next`, `#/lib/utils`, `./CheckpointMenu`, `./schema`

---

### webview-ui\src\components\chat\checkpoints\schema.ts
**Purpose:** Defines the Zod schema and TypeScript type for a checkpoint object.

**Exported Types:**
- `type Checkpoint`: from: string, to: string

**Exported Constants:**
- `checkpointSchema` = `z.object({ from: z.string(), to: z.string() })`

**Key Imports:** `zod`

---

### webview-ui\src\components\chat\CheckpointWarning.tsx
**Purpose:** Displays a warning message indicating that checkpoint initialization is in progress.

**Exported Functions:**
- `CheckpointWarning()` → `JSX.Element`

**Key Imports:** `react-i18next`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\chat\CloudTaskButton.tsx
**Purpose:** Renders a button to share a task to the cloud, generating a QR code.

**Exported Functions:**
- `CloudTaskButton({ item?: HistoryItem, disabled?: boolean })` → `JSX.Element`

**Exported Types:**
- `interface CloudTaskButtonProps`: item?: HistoryItem, disabled?: boolean

**Key Imports:** `react`, `react-i18next`, `lucide-react`, `qrcode`, `@roo-code/types`

---

### webview-ui\src\components\chat\CodebaseSearchResult.tsx
**Purpose:** Displays a single codebase search result with file path, lines, and score.

**Exported Functions:**
- `CodebaseSearchResult({ filePath: string, score: number, startLine: number, endLine: number, snippet: string, language: string })` → `JSX.Element`

**Exported Types:**
- `interface CodebaseSearchResultProps`: filePath: string, score: number, startLine: number, endLine: number, snippet: string

**Key Imports:** `react`, `react-i18next`, `@src/utils/vscode`, `#/components/ui`

---

### webview-ui\src\components\chat\CodebaseSearchResultsDisplay.tsx
**Purpose:** Displays expandable search results retrieved from the codebase index.

**Exported Functions:**
- `CodebaseSearchResultsDisplay({ results }: CodebaseSearchResultsDisplayProps)` → `JSX.Element`

**Exported Types:**
- `interface CodebaseSearchResultsDisplayProps`: results: Array<{ filePath: string, score: number, startLine: number, endLine: number, codeChunk: string }>

**Key Imports:** `react`, `./CodebaseSearchResult`, `react-i18next`

---

### webview-ui\src\components\chat\CodeIndexPopover.tsx
**Purpose:** Manages and displays the configuration and status of the codebase indexer.

**Key Imports:** `react`, `react-i18next`, `zod`, `@vscode/webview-ui-toolkit/react`, `@radix-ui/react-progress`

---

### webview-ui\src\components\chat\CommandExecution.tsx
**Purpose:** Displays the status, command, and output of a command execution block.

**Exported Functions:**
- `CommandExecution{ executionId: string, text?: string, icon?: JSX.Element | null, title?: JSX.Element | null }` → `JSX.Element`

**Key Imports:** `react`, `react-use`, `lucide-react`, `@roo-code/types`, `@roo/ExtensionMessage`

---

### webview-ui\src\components\chat\CommandExecutionError.tsx
**Purpose:** Renders an error message regarding disabled terminal shell integration.

**Exported Functions:**
- `CommandExecutionError()` → `JSX.Element`

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `../../utils/docLinks`

---

### webview-ui\src\components\chat\CommandPatternSelector.tsx
**Purpose:** Allows users to select and manage command patterns for execution approval.

**Exported Functions:**
- `CommandPatternSelector{ patterns: CommandPattern[], allowedCommands: string[], deniedCommands: string[], onAllowPatternChange: (pattern: string) => void, onDenyPatternChange: (pattern: string) => void }` → `JSX.Element`

**Key Imports:** `react`, `lucide-react`, `../../lib/utils`, `react-i18next`, `../ui/standard-tooltip`

---

### webview-ui\src\components\chat\ContextCondenseRow.tsx
**Purpose:** Displays an expandable row summarizing context condensation results and token savings.

**Exported Functions:**
- `ContextCondenseRowContextCondense` → `JSX.Element`

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `./Markdown`

---

### webview-ui\src\components\chat\ContextMenu.tsx
**Purpose:** Provides a dynamic context menu for selecting files, modes, or commands based on input query.

**Exported Functions:**
- `ContextMenuContextMenuProps` → `JSX.Element`

**Key Imports:** `react`, `vscode-material-icons`, `lucide-react`, `@roo-code/types`, `@roo/ExtensionMessage`

---

### webview-ui\src\components\chat\ContextWindowProgress.tsx
**Purpose:** Displays a progress bar visualizing token usage against the model's context window limit.

**Exported Functions:**
- `ContextWindowProgress{ contextWindow: number, contextTokens: number, maxTokens?: number }` → `JSX.Element`

**Key Imports:** `react`, `react-i18next`, `utils/format`, `utils/model-utils`, `components/ui`

---

### webview-ui\src\components\chat\ErrorRow.tsx
**Purpose:** Provides a unified, expandable component for displaying various chat error messages.

**Exported Functions:**
- `ErrorRowErrorRowProps` → `JSX.Element`

**Exported Types:**
- `interface ErrorRowProps`: type: "error" | "mistake_limit" | "api_failure" | "diff_error" | "streaming_failed" | "cancelled", title?: string, message: string, showCopyButton?: boolean, expandable?: boolean

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `lucide-react`, `@src/utils/clipboard`

---

### webview-ui\src\components\chat\FollowUpSuggest.tsx
**Purpose:** Displays suggested follow-up questions, optionally featuring an auto-approval countdown timer.

**Exported Functions:**
- `FollowUpSuggestFollowUpSuggestProps` → `JSX.Element`

**Key Imports:** `react`, `lucide-react`, `components/ui`, `@src/i18n/TranslationContext`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\chat\hooks\usePromptHistory.ts
**Purpose:** Manages prompt history navigation and state for the chat input field.

**Exported Functions:**
- `usePromptHistoryUsePromptHistoryProps` → `UsePromptHistoryReturn`

**Exported Types:**
- `interface UsePromptHistoryReturn`: historyIndex: number, setHistoryIndex: (index: number) => void, tempInput: string, promptHistory: string[], handleHistoryNavigation: (event: React.KeyboardEvent<HTMLTextAreaElement>, showContextMenu: boolean, isComposing: boolean) => boolean

**Key Imports:** `@roo-code/types`, `react`

---

### webview-ui\src\components\chat\IconButton.tsx
**Purpose:** Renders a standardized button displaying a codicon icon with optional tooltip and loading state.

**Exported Functions:**
- `IconButtonIconButtonProps` → `JSX.Element`

**Key Imports:** `@src/lib/utils`, `@src/components/ui`, `react`

---

### webview-ui\src\components\chat\IndexingStatusBadge.tsx
**Purpose:** Displays the current codebase indexing status and provides access to the index configuration popover.

**Exported Functions:**
- `IndexingStatusBadge{ className?: string }` → `JSX.Element`

**Key Imports:** `react`, `lucide-react`, `@src/lib/utils`, `@src/utils/vscode`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\chat\Markdown.tsx
**Purpose:** Renders markdown content, providing a copy button on hover for non-partial blocks.

**Exported Functions:**
- `Markdown{ markdown?: string, partial?: boolean }` → `JSX.Element`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@src/utils/clipboard`, `@src/components/ui`, `../common/MarkdownBlock`

---

### webview-ui\src\components\chat\McpExecution.tsx
**Functions:** `McpExecution`, `ResponseContainerInternal`

---

### webview-ui\src\components\chat\Mention.tsx
**Functions:** `Mention`

---

### webview-ui\src\components\chat\MessageModificationConfirmationDialog.tsx
---

### webview-ui\src\components\chat\ModeSelector.tsx
**Functions:** `ModeSelector`

---

### webview-ui\src\components\chat\ProfileViolationWarning.tsx
---

### webview-ui\src\components\chat\ProgressIndicator.tsx
**Functions:** `ProgressIndicator`

---

### webview-ui\src\components\chat\QueuedMessages.tsx
**Functions:** `QueuedMessages`, `getEditState`, `setEditState`, `handleSaveEdit`

---

### webview-ui\src\components\chat\ReasoningBlock.tsx
**Functions:** `ReasoningBlock`, `tick`, `handleToggle`

---

### webview-ui\src\components\chat\ShareButton.tsx
**Functions:** `ShareButton`, `handleMessage`, `handleShare`, `handleConnectToCloud`, `handleShareButtonClick`, `getShareButtonState`

---

### webview-ui\src\components\chat\SlashCommandItem.tsx
**Functions:** `handleEdit`, `handleDelete`

---

### webview-ui\src\components\chat\SlashCommandItemSimple.tsx
---

### webview-ui\src\components\chat\SystemPromptWarning.tsx
---

### webview-ui\src\components\chat\TaskActions.tsx
**Functions:** `TaskActions`

---

### webview-ui\src\components\chat\TaskHeader.tsx
**Functions:** `TaskHeader`

---

### webview-ui\src\components\chat\TodoListDisplay.tsx
**Functions:** `TodoListDisplay`, `getMostImportantTodoIcon`

---

### webview-ui\src\components\chat\UpdateTodoListToolBlock.tsx
**Functions:** `genId`, `handleContentChange`, `handleStatusChange`, `handleDelete`, `confirmDelete`, `cancelDelete`, `handleAdd`, `handleNewInputKeyDown`

---

### webview-ui\src\components\cloud\__tests__\CloudUpsellDialog.spec.tsx
---

### webview-ui\src\components\cloud\__tests__\CloudView.spec.tsx
---

### webview-ui\src\components\cloud\CloudAccountSwitcher.tsx
**Purpose:** Renders a cloud account switcher component for selecting organizations or creating a team.

**Exported Functions:**
- `CloudAccountSwitcher()` → `JSX.Element | null`

**Key Imports:** `react`, `lucide-react`, `@/components/ui/select`, `@src/i18n/TranslationContext`, `@src/utils/vscode`

---

### webview-ui\src\components\cloud\CloudUpsellDialog.tsx
**Purpose:** Presents a dialog to upsell cloud benefits and prompt the user to connect.

**Exported Functions:**
- `renderCloudBenefitsContent(t: any)` → `JSX.Element`
- `CloudUpsellDialog({ open, onOpenChange, onConnect }: CloudUpsellDialogProps)` → `JSX.Element`

**Exported Types:**
- `interface CloudUpsellDialogProps`: open, onOpenChange, onConnect

**Key Imports:** `react-i18next`, `@/components/ui`, `lucide-react`, `@radix-ui/react-dialog`, `../welcome/RooHero`

---

### webview-ui\src\components\cloud\CloudView.tsx
**Purpose:** Displays the cloud view, handling authentication, settings, and remote control.

**Exported Functions:**
- `CloudView({ userInfo, isAuthenticated, cloudApiUrl, onDone, organizations = [] }: CloudViewProps)` → `JSX.Element`

**Exported Types:**
- `type CloudViewProps`: userInfo, isAuthenticated, cloudApiUrl, onDone, organizations

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\cloud\OrganizationSwitcher.tsx
**Purpose:** Provides a component to switch between organizations within the cloud account.

**Exported Functions:**
- `OrganizationSwitcher({ userInfo, organizations, onOrganizationChange, cloudApiUrl }: OrganizationSwitcherProps)` → `JSX.Element`

**Exported Types:**
- `type OrganizationSwitcherProps`: userInfo, organizations, onOrganizationChange, cloudApiUrl

**Key Imports:** `react`, `lucide-react`, `@/components/ui/select`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\common\__mocks__\CodeBlock.tsx
---

### webview-ui\src\components\common\__mocks__\MarkdownBlock.tsx
---

### webview-ui\src\components\common\__tests__\CodeBlock.spec.tsx
---

### webview-ui\src\components\common\__tests__\DismissibleUpsell.spec.tsx
**Functions:** `makeUpsellVisible`

---

### webview-ui\src\components\common\__tests__\FormattedTextField.spec.tsx
---

### webview-ui\src\components\common\__tests__\ImageViewer.spec.tsx
---

### webview-ui\src\components\common\__tests__\MarkdownBlock.spec.tsx
---

### webview-ui\src\components\common\CodeAccordian.tsx
**Purpose:** Renders an expandable code block with syntax highlighting and optional file path.

**Exported Functions:**
- `CodeAccordian({ path, code = "", language, progressStatus, isLoading, isExpanded, isFeedback, onToggleExpand, header, onJumpToFile }: CodeAccordianProps)` → `JSX.Element`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/utils/getLanguageFromPath`, `@src/utils/removeLeadingNonAlphanumeric`

---

### webview-ui\src\components\common\CodeBlock.tsx
**Purpose:** Displays a syntax-highlighted code block with copy functionality and scroll management.

**Exported Functions:**
- `pre(props: any)` → `any`
- `code(props: any)` → `any`
- `line(props: any)` → `any`

**Exported Constants:**
- `CODE_BLOCK_BG_COLOR` = `"var(--vscode-editor-background, --vscode-sideBar-background, rgb(30 30 30))"`
- `WRAPPER_ALPHA` = `"cc"`
- `SCROLL_SNAP_TOLERANCE` = `20`

**Key Imports:** `react`, `styled-components`, `@src/utils/clipboard`, `@src/utils/highlighter`, `shiki`, `hast-util-to-jsx-runtime`

---

### webview-ui\src\components\common\DecoratedVSCodeTextField.tsx
**Purpose:** Enhances VSCodeTextField with left and right nodes for flexible UI composition.

**Exported Functions:**
- `VSCodeTextFieldWithNodesInner(props: VSCodeTextFieldWithNodesProps, forwardedRef: React.Ref<HTMLInputElement>)` → `JSX.Element`

**Exported Types:**
- `interface VSCodeTextFieldWithNodesProps`: leftNodes, rightNodes

**Key Imports:** `@/lib/utils`, `@vscode/webview-ui-toolkit/react`, `react`

---

### webview-ui\src\components\common\DismissibleUpsell.tsx
**Purpose:** Renders a dismissible upsell component with customizable content and dismissal tracking.

**Exported Functions:**
- `DismissibleUpsell({ upsellId, className, icon, children, variant = "default", onDismiss, onClick, dismissOnClick = false }: DismissibleUpsellProps)` → `React.MemoExoticComponent<({ upsellId, className, icon, children, variant, onDismiss, onClick, dismissOnClick }: DismissibleUpsellProps) => JSX.Element | null>`

**Key Imports:** `react`, `@src/utils/vscode`, `@src/i18n/TranslationContext`, `@src/utils/TelemetryClient`, `@roo-code/types`

---

### webview-ui\src\components\common\FormattedTextField.tsx
**Purpose:** Renders a text field with input formatting and parsing capabilities.

**Exported Types:**
- `interface InputFormatter`: parse, format, filter
- `interface FormattedTextFieldProps`: value, onValueChange, formatter

**Key Imports:** `react`, `./DecoratedVSCodeTextField`

---

### webview-ui\src\components\common\IconButton.tsx
**Purpose:** Displays an icon button with optional tooltip and click handlers.

**Exported Functions:**
- `IconButton({ icon, onClick, onMouseDown, onMouseUp, onMouseLeave, title, size = "medium", variant = "default" }: IconButtonProps)` → `JSX.Element`

**Exported Types:**
- `interface IconButtonProps`: icon, onClick, onMouseDown, onMouseUp, onMouseLeave, title, size, variant

**Key Imports:** `react`, `@/components/ui`

---

### webview-ui\src\components\common\ImageBlock.tsx
**Purpose:** Renders an image using URI, path, or base64 data.

**Exported Functions:**
- `ImageBlock({ imageUri, imagePath, imageData, path }: ImageBlockProps)` → `JSX.Element`

**Exported Types:**
- `interface ImageBlockProps`: imageUri, imagePath, imageData, path

**Key Imports:** `react`, `./ImageViewer`

---

### webview-ui\src\components\common\ImageViewer.tsx
**Purpose:** Displays an image with zoom, copy, save, and open controls.

**Exported Functions:**
- `ImageViewer({ imageUri, imagePath, alt = "Generated image", showControls = true, className = "" }: ImageViewerProps)` → `JSX.Element`

**Exported Types:**
- `interface ImageViewerProps`: imageUri, imagePath, alt, showControls, className

**Exported Constants:**
- `MIN_ZOOM` = `0.5`
- `MAX_ZOOM` = `20`

**Key Imports:** `react`, `@src/utils/clipboard`, `@src/i18n/TranslationContext`, `@src/utils/vscode`, `./MermaidActionButtons`, `./Modal`, `./TabButton`, `./IconButton`, `./ZoomControls`, `@/components/ui`

---

### webview-ui\src\components\common\MarkdownBlock.tsx
**Purpose:** Renders markdown content with support for code blocks and math.

**Exported Types:**
- `interface MarkdownBlockProps`: markdown

**Key Imports:** `react`, `react-markdown`, `styled-components`, `unist-util-visit`, `rehype-katex`, `remark-math`, `remark-gfm`, `@src/utils/vscode`, `./CodeBlock`, `./MermaidBlock`

---

### webview-ui\src\components\common\MermaidActionButtons.tsx
**Purpose:** Provides action buttons for Mermaid diagrams (zoom, copy, save, view code).

**Exported Functions:**
- `MermaidActionButtons({ onZoom, onZoomIn, onZoomOut, onCopy, onSave, onViewCode, onClose, copyFeedback, showZoomControls = false, zoomLevel }: MermaidActionButtonsProps)` → `JSX.Element`

**Exported Types:**
- `interface MermaidActionButtonsProps`: onZoom, onZoomIn, onZoomOut, onCopy, onSave, onViewCode, onClose, copyFeedback, showZoomControls, zoomLevel

**Key Imports:** `react`, `@src/i18n/TranslationContext`, `./IconButton`, `./ZoomControls`, `@/components/ui`

---

### webview-ui\src\components\common\MermaidBlock.tsx
**Purpose:** Renders Mermaid diagrams from code with dynamic theming.

**Exported Functions:**
- `MermaidBlock()` → `JSX.Element`

**Key Imports:** `react`, `mermaid`, `styled-components`, `@src/utils/useDebounceEffect`, `@src/utils/vscode`, `@src/i18n/TranslationContext`, `@src/utils/clipboard`, `./CodeBlock`, `./MermaidButton`

---

### webview-ui\src\components\common\MermaidButton.tsx
**Purpose:** Button to display a Mermaid diagram in a modal with interactive controls.

**Exported Functions:**
- `MermaidButton({ containerRef, code, isLoading, svgToPng, children }: MermaidButtonProps)` → `JSX.Element`

**Exported Types:**
- `interface MermaidButtonProps`: containerRef, code, isLoading, svgToPng, children

**Exported Constants:**
- `MIN_ZOOM` = `0.5`
- `MAX_ZOOM` = `20`

**Key Imports:** `react`, `@src/utils/clipboard`, `@src/i18n/TranslationContext`, `@src/utils/vscode`, `./MermaidActionButtons`, `./Modal`, `./TabButton`, `./IconButton`, `./ZoomControls`, `@/components/ui`

---

### webview-ui\src\components\common\Modal.tsx
**Purpose:** A reusable modal component with backdrop and close functionality.

**Exported Functions:**
- `Modal({ isOpen, onClose, children, className = "" }: ModalProps)` → `JSX.Element | null`

**Exported Types:**
- `interface ModalProps`: isOpen, onClose, children, className

---

### webview-ui\src\components\common\Tab.tsx
**Purpose:** Provides tabbed content structure with header, content, and list components.

**Exported Functions:**
- `Tab({ className, children, ...props }: TabProps)` → `JSX.Element`
- `TabHeader({ className, children, ...props }: TabProps)` → `JSX.Element`
- `TabContent({ className, children, ...props }, ref: React.Ref<HTMLDivElement>)` → `JSX.Element`

**Exported Types:**
- `type TabProps`

**Key Imports:** `react`, `@/context/ExtensionStateContext`, `@/lib/utils`

---

### webview-ui\src\components\common\TabButton.tsx
**Purpose:** A clickable tab button with an icon and label for navigation.

**Exported Functions:**
- `TabButton({ icon, label, isActive, onClick }: TabButtonProps)` → `JSX.Element`

**Exported Types:**
- `interface TabButtonProps`: icon, label, isActive, onClick

---

### webview-ui\src\components\common\TelemetryBanner.tsx
**Purpose:** Displays a banner to inform users about telemetry settings.

**Exported Functions:**
- `TelemetryBanner()` → `JSX.Element | null`

**Exported Types:**
- `type TelemetrySetting`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/utils/vscode`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\common\Thumbnails.tsx
**Purpose:** Renders a grid of image thumbnails with optional delete functionality.

**Exported Functions:**
- `Thumbnails({ images, style, setImages, onHeightChange }: ThumbnailsProps)` → `JSX.Element`

**Exported Types:**
- `interface ThumbnailsProps`: images, style, setImages, onHeightChange

**Key Imports:** `react`, `react-use`, `@src/utils/vscode`

---

### webview-ui\src\components\common\ToolUseBlock.tsx
**Purpose:** Component for displaying tool usage information with a header.

**Exported Functions:**
- `ToolUseBlock({ className, ...props }: React.HTMLAttributes<HTMLDivElement>)` → `JSX.Element`
- `ToolUseBlockHeader({ className, ...props }: React.HTMLAttributes<HTMLDivElement>)` → `JSX.Element`

**Key Imports:** `@/lib/utils`

---

### webview-ui\src\components\common\VersionIndicator.tsx
**Purpose:** Displays the application version with a click handler.

**Exported Functions:**
- `VersionIndicator: React.FC<VersionIndicatorProps>` → `JSX.Element`

**Exported Types:**
- `interface VersionIndicatorProps`: onClick, className

**Key Imports:** `react`, `react-i18next`, `@roo/package`

---

### webview-ui\src\components\common\VSCodeButtonLink.tsx
**Purpose:** Creates a link that renders as a VSCode button.

**Exported Functions:**
- `VSCodeButtonLink({ href, children, ...props }: VSCodeButtonLinkProps)` → `JSX.Element`

**Exported Types:**
- `interface VSCodeButtonLinkProps`: href, children

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\common\ZoomControls.tsx
**Purpose:** Provides zoom in/out buttons with optional continuous zoom functionality.

**Exported Functions:**
- `ZoomControls({ zoomLevel, zoomInTitle, zoomOutTitle, useContinuousZoom = false, adjustZoom, zoomInStep = 0.1, zoomOutStep = -0.1, onZoomIn, onZoomOut }: ZoomControlsProps)` → `JSX.Element`

**Exported Types:**
- `interface ZoomControlsProps`: zoomLevel, zoomInTitle, zoomOutTitle, useContinuousZoom, adjustZoom, zoomInStep, zoomOutStep, onZoomIn, onZoomOut

**Key Imports:** `./IconButton`, `react`, `@/components/ui`

---

### webview-ui\src\components\ErrorBoundary.tsx
**Purpose:** Renders a fallback UI when components throw errors during rendering.

**Exported Functions:**
- `getDerivedStateFromError(error: unknown)` → `Pick<ErrorState, 'error' | 'timestamp'>`
- `componentDidCatch(error: Error, errorInfo: React.ErrorInfo)` → `Promise<void>`

**Exported Types:**
- `type ErrorProps`: children: React.ReactNode, & WithTranslation
- `type ErrorState`: error?: string, componentStack?: string | null, timestamp?: number

**Key Imports:** `react`, `@src/utils/TelemetryClient`, `react-i18next`, `@src/utils/sourceMapUtils`

---

### webview-ui\src\components\history\__tests__\BatchDeleteTaskDialog.spec.tsx
---

### webview-ui\src\components\history\__tests__\CopyButton.spec.tsx
---

### webview-ui\src\components\history\__tests__\DeleteButton.spec.tsx
---

### webview-ui\src\components\history\__tests__\DeleteTaskDialog.spec.tsx
---

### webview-ui\src\components\history\__tests__\ExportButton.spec.tsx
---

### webview-ui\src\components\history\__tests__\HistoryPreview.spec.tsx
---

### webview-ui\src\components\history\__tests__\HistoryView.spec.tsx
---

### webview-ui\src\components\history\__tests__\TaskItem.spec.tsx
---

### webview-ui\src\components\history\__tests__\TaskItemFooter.spec.tsx
---

### webview-ui\src\components\history\__tests__\useTaskSearch.spec.tsx
---

### webview-ui\src\components\history\BatchDeleteTaskDialog.tsx
**Purpose:** Displays a confirmation dialog for deleting multiple history tasks.

**Exported Functions:**
- `BatchDeleteTaskDialog({ taskIds, ...props }: BatchDeleteTaskDialogProps)` → `JSX.Element | null`

**Exported Types:**
- `interface BatchDeleteTaskDialogProps`: taskIds: string[], {...props}: AlertDialogProps

**Key Imports:** `react`, `@/i18n/TranslationContext`, `@/components/ui`, `@/utils/vscode`, `@radix-ui/react-alert-dialog`

---

### webview-ui\src\components\history\CopyButton.tsx
**Purpose:** Provides a button to copy a task string to the clipboard.

**Exported Functions:**
- `CopyButton({ itemTask }: CopyButtonProps)` → `JSX.Element`

**Exported Types:**
- `type CopyButtonProps`: itemTask: string

**Key Imports:** `react`, `@/components/ui/hooks`, `@/components/ui`, `@/i18n/TranslationContext`, `@/lib/utils`

---

### webview-ui\src\components\history\DeleteButton.tsx
**Purpose:** Renders a button to delete a task, optionally triggering VS Code.

**Exported Functions:**
- `DeleteButton({ itemId, onDelete }: DeleteButtonProps)` → `JSX.Element`

**Exported Types:**
- `type DeleteButtonProps`: itemId: string, onDelete?: (taskId: string) => void

**Key Imports:** `react`, `@/components/ui`, `@/i18n/TranslationContext`, `@/utils/vscode`

---

### webview-ui\src\components\history\DeleteTaskDialog.tsx
**Purpose:** Shows a confirmation dialog before deleting a specific history task.

**Exported Functions:**
- `DeleteTaskDialog({ taskId, ...props }: DeleteTaskDialogProps)` → `JSX.Element | null`

**Exported Types:**
- `interface DeleteTaskDialogProps`: taskId: string, {...props}: AlertDialogProps

**Key Imports:** `react`, `react-use`, `@radix-ui/react-alert-dialog`, `@/components/ui`, `@/i18n/TranslationContext`, `@/utils/vscode`

---

### webview-ui\src\components\history\ExportButton.tsx
**Purpose:** Creates a button to export a specific history task via VS Code.

**Exported Functions:**
- `ExportButton({ itemId }: { itemId: string })` → `JSX.Element`

**Key Imports:** `@/utils/vscode`, `@/components/ui`, `@/i18n/TranslationContext`, `react`

---

### webview-ui\src\components\history\HistoryPreview.tsx
**Purpose:** Displays a compact preview of the three most recent history tasks.

**Exported Functions:**
- `HistoryPreview()` → `JSX.Element | null`

**Key Imports:** `react`, `@src/utils/vscode`, `@src/i18n/TranslationContext`, `./useTaskSearch`, `./TaskItem`

---

### webview-ui\src\components\history\HistoryView.tsx
**Purpose:** Renders the main view for searching, sorting, and managing history tasks.

**Exported Functions:**
- `HistoryView{ onDone }: HistoryViewProps` → `JSX.Element`

**Exported Types:**
- `type HistoryViewProps`: onDone: () => void
- `type SortOption`: newest, oldest, mostExpensive, mostTokens, mostRelevant

**Key Imports:** `react`, `react`, `./DeleteTaskDialog`, `./BatchDeleteTaskDialog`, `react-virtuoso`, `@vscode/webview-ui-toolkit/react`, `@/components/ui`, `@/i18n/TranslationContext`, `../common/Tab`, `./useTaskSearch`, `./TaskItem`

---

### webview-ui\src\components\history\TaskItem.tsx
**Purpose:** Displays an individual history task item with interaction options.

**Exported Functions:**
- `TaskItem({ item, variant, showWorkspace, isSelectionMode, isSelected, onToggleSelection, onDelete, className, }: TaskItemProps)` → `JSX.Element`

**Exported Types:**
- `interface DisplayHistoryItem`: highlight?: string, extends HistoryItem
- `interface TaskItemProps`: item: DisplayHistoryItem, variant: "compact" | "full", showWorkspace?: boolean, isSelectionMode?: boolean, isSelected?: boolean

**Key Imports:** `react`, `@roo-code/types`, `@/utils/vscode`, `@/lib/utils`, `@/components/ui/checkbox`, `./TaskItemFooter`

---

### webview-ui\src\components\history\TaskItemFooter.tsx
**Purpose:** Renders metadata and action buttons below a history task item.

**Exported Types:**
- `interface TaskItemFooterProps`: item: HistoryItem, variant: "compact" | "full", isSelectionMode?: boolean, onDelete?: (taskId: string) => void

**Key Imports:** `react`, `@roo-code/types`, `@/utils/format`, `./CopyButton`, `./ExportButton`, `./DeleteButton`, `../ui/standard-tooltip`

---

### webview-ui\src\components\history\useTaskSearch.ts
**Purpose:** Manages state for searching, filtering, and sorting the task history.

**Exported Functions:**
- `useTaskSearch()` → `{ tasks: any[], searchQuery: string, setSearchQuery: any, sortOption: SortOption, setSortOption: any, setLastNonRelevantSort: any, showAllWorkspaces: boolean, setShowAllWorkspaces: any }`

**Exported Types:**
- `type SortOption`: newest, oldest, mostExpensive, mostTokens, mostRelevant

**Key Imports:** `react`, `fzf`, `@/utils/highlight`, `@/context/ExtensionStateContext`

---

### webview-ui\src\components\human-relay\HumanRelayDialog.tsx
**Purpose:** Displays a prompt and collects user input for human relay tasks.

**Exported Types:**
- `interface HumanRelayDialogProps`: isOpen: boolean, onClose: () => void, requestId: string, promptText: string, onSubmit: (requestId: string, text: string) => void

**Key Imports:** `react`, `../ui/button`, `../ui/dialog`, `../ui/textarea`, `../ui/hooks`

---

### webview-ui\src\components\marketplace\__tests__\MarketplaceListView.spec.tsx
**Functions:** `renderWithProviders`

---

### webview-ui\src\components\marketplace\__tests__\MarketplaceView.spec.tsx
---

### webview-ui\src\components\marketplace\__tests__\MarketplaceViewStateManager.spec.ts
---

### webview-ui\src\components\marketplace\components\__tests__\MarketplaceInstallModal-optional-params.spec.tsx
---

### webview-ui\src\components\marketplace\components\__tests__\MarketplaceInstallModal.spec.tsx
---

### webview-ui\src\components\marketplace\components\__tests__\MarketplaceItemCard.spec.tsx
**Functions:** `renderWithProviders`

---

### webview-ui\src\components\marketplace\components\MarketplaceInstallModal.tsx
**Purpose:** Manages the installation process for marketplace items, handling parameters and scope.

**Exported Types:**
- `interface MarketplaceInstallModalProps`: item: MarketplaceItem | null, isOpen: boolean, onClose: () => void, hasWorkspace: boolean

**Key Imports:** `react`, `@roo-code/types`, `@/utils/vscode`, `@/i18n/TranslationContext`, `@/components/ui/dialog`

---

### webview-ui\src\components\marketplace\components\MarketplaceItemCard.tsx
**Purpose:** Displays a marketplace item, allowing installation, removal, and filtering by tags.

**Exported Types:**
- `interface ItemInstalledMetadata`: type: string
- `interface MarketplaceItemCardProps`: item: MarketplaceItem, filters: ViewState["filters"], setFilters: (filters: Partial<ViewState["filters"]>) => void, installed: { project: ItemInstalledMetadata | undefined; global: ItemInstalledMetadata | undefined; }

**Key Imports:** `react`, `@roo-code/types`, `@/utils/vscode`, `@/utils/TelemetryClient`, `../MarketplaceViewStateManager`

---

### webview-ui\src\components\marketplace\IssueFooter.tsx
**Purpose:** Renders a footer component linking users to open a GitHub issue.

**Exported Types:**
- `type IssueFooter`

**Key Imports:** `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\marketplace\MarketplaceListView.tsx
**Purpose:** Displays a filterable list of marketplace items based on the current view state.

**Exported Functions:**
- `MarketplaceListView({ stateManager, allTags, filteredTags, filterByType }: MarketplaceListViewProps)` → `JSX.Element`

**Exported Types:**
- `interface MarketplaceListViewProps`: stateManager: MarketplaceViewStateManager, allTags: string[], filteredTags: string[], filterByType?: "mcp" | "mode"

**Key Imports:** `react`, `@/components/ui/input`, `@/components/ui/button`, `./MarketplaceViewStateManager`, `./useStateManager`

---

### webview-ui\src\components\marketplace\MarketplaceView.tsx
**Purpose:** Provides the main container for viewing and interacting with marketplace items across tabs.

**Exported Functions:**
- `MarketplaceView({ stateManager, onDone, targetTab }: MarketplaceViewProps)` → `JSX.Element`

**Exported Types:**
- `interface MarketplaceViewProps`: onDone?: () => void, stateManager: MarketplaceViewStateManager, targetTab?: "mcp" | "mode"

**Key Imports:** `react`, `./MarketplaceViewStateManager`, `./useStateManager`, `@/utils/vscode`, `./MarketplaceListView`

---

### webview-ui\src\components\marketplace\MarketplaceViewStateManager.ts
**Purpose:** Manages the complex state and transitions for the marketplace view interface.

**Exported Types:**
- `interface ViewState`: allItems: MarketplaceItem[], organizationMcps: MarketplaceItem[], displayItems?: MarketplaceItem[], isFetching: boolean, activeTab: "mcp" | "mode"
- `class MarketplaceViewStateManager`

**Key Imports:** `@roo-code/types`, `../../utils/vscode`, `../../../../src/shared/WebviewMessage`, `../../../../src/shared/ExtensionMessage`

---

### webview-ui\src\components\marketplace\useStateManager.ts
**Purpose:** Initializes and manages the reactive state derived from the MarketplaceViewStateManager instance.

**Exported Functions:**
- `useStateManager(existingManager?: MarketplaceViewStateManager)` → `[MarketplaceViewStateManager, ViewState]`

**Key Imports:** `react`, `./MarketplaceViewStateManager`

---

### webview-ui\src\components\mcp\__tests__\McpToolRow.spec.tsx
**Functions:** `MockVSCodeCheckbox`

---

### webview-ui\src\components\mcp\McpEnabledToggle.tsx
**Purpose:** Provides a toggle switch to enable or disable the MCP feature globally.

**Exported Functions:**
- `default()` → `JSX.Element`

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `react`, `@src/context/ExtensionStateContext`, `@src/i18n/TranslationContext`, `@src/utils/vscode`

---

### webview-ui\src\components\mcp\McpErrorRow.tsx
**Purpose:** Renders a single row displaying details of an MCP error entry.

**Exported Functions:**
- `McpErrorRow({ error }: McpErrorRowProps)` → `JSX.Element`

**Exported Types:**
- `type McpErrorRowProps`: error: McpErrorEntry

**Key Imports:** `react`, `date-fns`, `@roo/mcp`

---

### webview-ui\src\components\mcp\McpResourceRow.tsx
**Purpose:** Displays details for a single MCP resource or resource template.

**Exported Functions:**
- `default({ item }: McpResourceRowProps)` → `JSX.Element`

**Exported Types:**
- `type McpResourceRowProps`: item: McpResource | McpResourceTemplate

**Key Imports:** `@roo/mcp`

---

### webview-ui\src\components\mcp\McpToolRow.tsx
**Purpose:** Renders a row displaying an MCP tool with options for enabling and allowing access.

**Exported Functions:**
- `McpToolRow({ tool, serverName, serverSource, alwaysAllowMcp, isInChatContext }: McpToolRowProps)` → `JSX.Element`

**Exported Types:**
- `type McpToolRowProps`: tool: McpTool, serverName?: string, serverSource?: "global" | "project", alwaysAllowMcp?: boolean, isInChatContext?: boolean

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `@roo/mcp`, `@src/i18n/TranslationContext`, `@src/utils/vscode`, `@/components/ui`

---

### webview-ui\src\components\mcp\McpView.tsx
**Purpose:** Displays the main view for managing and configuring MCP servers and settings.

**Exported Functions:**
- `McpView({ onDone }: McpViewProps)` → `JSX.Element`

**Exported Types:**
- `type McpViewProps`: onDone: () => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo/mcp`, `@src/context/ExtensionStateContext`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\modes\__tests__\ModesView.spec.tsx
**Functions:** `renderPromptsView`

---

### webview-ui\src\components\modes\DeleteModeDialog.tsx
**Purpose:** Renders a confirmation dialog for deleting a custom AI mode configuration.

**Exported Functions:**
- `DeleteModeDialog({ open, onOpenChange, modeToDelete, onConfirm }: DeleteModeDialogProps)` → `React.FC<DeleteModeDialogProps>`

**Exported Types:**
- `interface DeleteModeDialogProps`: open: boolean, onOpenChange: (open: boolean) => void, modeToDelete: { slug: string, name: string, source?: string, rulesFolderPath?: string } | null, onConfirm: () => void

**Key Imports:** `react`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\modes\ModesView.tsx
**Purpose:** Provides the main interface for viewing, configuring, and managing AI modes.

**Exported Functions:**
- `ModesView()` → `JSX.Element`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/modes`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\components\settings\__tests__\ApiConfigManager.spec.tsx
**Functions:** `getRenameForm`, `getDialogContent`

---

### webview-ui\src\components\settings\__tests__\ApiOptions.provider-filtering.spec.tsx
**Functions:** `renderWithProviders`

---

### webview-ui\src\components\settings\__tests__\ApiOptions.spec.tsx
**Functions:** `renderApiOptions`

---

### webview-ui\src\components\settings\__tests__\AutoApproveToggle.spec.tsx
---

### webview-ui\src\components\settings\__tests__\ContextManagementSettings.spec.tsx
---

### webview-ui\src\components\settings\__tests__\ImageGenerationSettings.spec.tsx
---

### webview-ui\src\components\settings\__tests__\MaxCostInput.spec.tsx
---

### webview-ui\src\components\settings\__tests__\MaxRequestsInput.spec.tsx
---

### webview-ui\src\components\settings\__tests__\ModelPicker.deprecated.spec.tsx
---

### webview-ui\src\components\settings\__tests__\ModelPicker.spec.tsx
**Functions:** `renderModelPicker`

---

### webview-ui\src\components\settings\__tests__\SettingsView.change-detection.spec.tsx
**Functions:** `createExtensionState`

---

### webview-ui\src\components\settings\__tests__\SettingsView.spec.tsx
**Functions:** `handleClick`, `mockPostMessage`, `renderSettingsView`, `activateTab`

---

### webview-ui\src\components\settings\__tests__\SettingsView.unsaved-changes.spec.tsx
**Functions:** `handleUserChange`

---

### webview-ui\src\components\settings\__tests__\SlashCommandsSettings.spec.tsx
**Functions:** `renderSlashCommandsSettings`

---

### webview-ui\src\components\settings\__tests__\TemperatureControl.spec.tsx
---

### webview-ui\src\components\settings\__tests__\ThinkingBudget.spec.tsx
---

### webview-ui\src\components\settings\__tests__\TodoListSettingsControl.spec.tsx
---

### webview-ui\src\components\settings\__tests__\UISettings.spec.tsx
---

### webview-ui\src\components\settings\About.tsx
**Functions:** `About`

---

### webview-ui\src\components\settings\ApiConfigManager.tsx
**Functions:** `ApiConfigManager`, `resetCreateState`, `resetRenameState`, `handleSelectConfig`, `handleAdd`, `handleStartRename`, `handleCancel`, `handleSave`, `handleNewProfileSave`, `handleDelete`

---

### webview-ui\src\components\settings\ApiErrorMessage.tsx
**Functions:** `ApiErrorMessage`

---

### webview-ui\src\components\settings\ApiOptions.tsx
**Functions:** `ApiOptions`, `validateAndResetModel`

---

### webview-ui\src\components\settings\AutoApproveSettings.tsx
**Functions:** `AutoApproveSettings`, `handleAddCommand`, `handleAddDeniedCommand`

---

### webview-ui\src\components\settings\AutoApproveToggle.tsx
**Functions:** `AutoApproveToggle`

---

### webview-ui\src\components\settings\BrowserSettings.tsx
**Functions:** `BrowserSettings`, `handleMessage`, `testConnection`

---

### webview-ui\src\components\settings\CheckpointSettings.tsx
**Functions:** `CheckpointSettings`

---

### webview-ui\src\components\settings\ConsecutiveMistakeLimitControl.tsx
---

### webview-ui\src\components\settings\constants.ts
---

### webview-ui\src\components\settings\ContextManagementSettings.tsx
**Functions:** `ContextManagementSettings`, `getCurrentThresholdValue`, `handleThresholdChange`

---

### webview-ui\src\components\settings\DiffSettingsControl.tsx
---

### webview-ui\src\components\settings\ExperimentalFeature.tsx
**Functions:** `ExperimentalFeature`

---

### webview-ui\src\components\settings\ExperimentalSettings.tsx
**Functions:** `ExperimentalSettings`

---

### webview-ui\src\components\settings\ImageGenerationSettings.tsx
**Purpose:** Renders image generation settings using React components.

**Exported Functions:**
- `ImageGenerationSettingsImageGenerationSettingsProps` → `any`
- `handleApiKeyChange` → ``
- `handleModelChange` → ``

**Exported Types:**
- `interface ImageGenerationSettingsProps`: enabled: boolean, onChange: (enabled: boolean) => void, openRouterImageApiKey?: string, openRouterImageGenerationSelectedModel?: string, setOpenRouterImageApiKey: (apiKey: string) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@/i18n/TranslationContext`, `useState`, `useEffect`

---

### webview-ui\src\components\settings\LanguageSettings.tsx
**Purpose:** Displays and manages language settings within the UI.

**Exported Functions:**
- `LanguageSettingsLanguageSettingsProps` → `any`

**Exported Types:**
- `type LanguageSettingsProps`: language: string, setCachedStateField: SetCachedStateField<"language">, className?: string, ...props: HTMLAttributes<HTMLDivElement>

**Key Imports:** `react`, `@roo-code/types`, `@roo/language`, `@src/lib/utils`, `@src/components/ui`

---

### webview-ui\src\components\settings\MaxCostInput.tsx
**Purpose:** Provides an input field for setting the maximum API cost.

**Exported Functions:**
- `MaxCostInputMaxCostInputProps` → `any`

**Exported Types:**
- `interface MaxCostInputProps`: allowedMaxCost?: number, onValueChange: (value: number | undefined) => void

**Key Imports:** `react-i18next`, `@/utils/vscode`, `react`, `FormattedTextField`, `unlimitedDecimalFormatter`

---

### webview-ui\src\components\settings\MaxLimitInputs.tsx
**Purpose:** Renders inputs for setting maximum request and cost limits.

**Exported Functions:**
- `MaxLimitInputsMaxLimitInputsProps` → `React.FC<MaxLimitInputsProps>`

**Exported Types:**
- `interface MaxLimitInputsProps`: allowedMaxRequests?: number, allowedMaxCost?: number, onMaxRequestsChange: (value: number | undefined) => void, onMaxCostChange: (value: number | undefined) => void

**Key Imports:** `react-i18next`, `MaxRequestsInput`, `MaxCostInput`, `React`

---

### webview-ui\src\components\settings\MaxRequestsInput.tsx
**Purpose:** Provides an input field for setting the maximum API requests.

**Exported Functions:**
- `MaxRequestsInputMaxRequestsInputProps` → `any`

**Exported Types:**
- `interface MaxRequestsInputProps`: allowedMaxRequests?: number, onValueChange: (value: number | undefined) => void

**Key Imports:** `react-i18next`, `@/utils/vscode`, `react`, `FormattedTextField`, `unlimitedIntegerFormatter`

---

### webview-ui\src\components\settings\ModelDescriptionMarkdown.tsx
**Purpose:** Displays model descriptions using Markdown with expand/collapse functionality.

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `react`, `react-remark`, `@/lib/utils`

---

### webview-ui\src\components\settings\ModelInfoView.tsx
**Purpose:** Renders detailed information about a selected model.

**Exported Functions:**
- `ModelInfoViewModelInfoViewProps` → `any`
- `fmtn?: number` → `any`
- `ModelInfoSupportsItem` → ``

**Exported Types:**
- `type ModelInfoViewProps`: apiProvider?: string, selectedModelId: string, modelInfo?: ModelInfo, isDescriptionExpanded: boolean, setIsDescriptionExpanded: (isExpanded: boolean) => void

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/utils/formatPrice`, `@src/lib/utils`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\ModelPicker.tsx
**Purpose:** Provides a component for selecting a model from a list.

**Exported Functions:**
- `ModelPickerModelPickerProps` → `any`

**Exported Types:**
- `type ModelIdKey`: glamaModelId, openRouterModelId, unboundModelId, requestyModelId
- `interface ModelPickerProps`: defaultModelId: string, models: Record<string, ModelInfo> | null, modelIdKey: ModelIdKey, serviceName: string

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `react-i18next`, `lucide-react`, `@roo-code/types`

---

### webview-ui\src\components\settings\NotificationSettings.tsx
**Purpose:** Renders notification settings including TTS and sound options.

**Exported Functions:**
- `NotificationSettingsNotificationSettingsProps` → `any`

**Exported Types:**
- `type NotificationSettingsProps`: ttsEnabled?: boolean, ttsSpeed?: number, soundEnabled?: boolean, soundVolume?: number, setCachedStateField: SetCachedStateField<"ttsEnabled" | "ttsSpeed" | "soundEnabled" | "soundVolume">

**Key Imports:** `react`, `@/i18n/TranslationContext`, `@vscode/webview-ui-toolkit/react`, `lucide-react`, `SetCachedStateField`

---

### webview-ui\src\components\settings\PromptsSettings.tsx
**Purpose:** Manages and renders settings related to prompts.

**Exported Functions:**
- `PromptsSettingsPromptsSettingsProps` → `any`
- `handler` → ``
- `updateSupportPrompt` → ``
- `handleSupportReset` → ``
- `handleTestEnhancement` → ``

**Exported Types:**
- `interface PromptsSettingsProps`: customSupportPrompts: Record<string, string | undefined>, setCustomSupportPrompts: (prompts: Record<string, string | undefined>) => void, includeTaskHistoryInEnhance?: boolean, setIncludeTaskHistoryInEnhance?: (value: boolean) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo/support-prompt`, `@src/utils/vscode`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\__tests__\Bedrock.spec.tsx
---

### webview-ui\src\components\settings\providers\__tests__\Gemini.spec.tsx
---

### webview-ui\src\components\settings\providers\__tests__\HuggingFace.spec.tsx
---

### webview-ui\src\components\settings\providers\__tests__\OpenAICompatible.spec.tsx
---

### webview-ui\src\components\settings\providers\__tests__\Vertex.spec.tsx
---

### webview-ui\src\components\settings\providers\Anthropic.tsx
**Purpose:** Renders and manages Anthropic provider-specific settings.

**Exported Functions:**
- `AnthropicAnthropicProps` → `any`

**Exported Types:**
- `type AnthropicProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Bedrock.tsx
**Purpose:** Renders and manages Bedrock provider-specific settings.

**Exported Functions:**
- `BedrockBedrockProps` → `any`

**Exported Types:**
- `type BedrockProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, selectedModelInfo?: ModelInfo

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\BedrockCustomArn.tsx
**Purpose:** Provides a custom ARN input field for Bedrock settings.

**Exported Functions:**
- `BedrockCustomArnBedrockCustomArnProps` → `any`

**Exported Types:**
- `type BedrockCustomArnProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/utils/validate`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Cerebras.tsx
**Purpose:** Renders and manages Cerebras provider-specific settings.

**Exported Functions:**
- `CerebrasCerebrasProps` → `any`

**Exported Types:**
- `type CerebrasProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Chutes.tsx
**Purpose:** Renders and manages Chutes provider-specific settings.

**Exported Functions:**
- `ChutesChutesProps` → `any`

**Exported Types:**
- `type ChutesProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\ClaudeCode.tsx
**Purpose:** Renders Claude Code settings, handling input changes for the Claude Code path.

**Exported Functions:**
- `handleInputChange(e: Event | React.FormEvent<HTMLElement>)` → `void`

**Exported Types:**
- `interface ClaudeCode`
- `interface ClaudeCodeProps`: apiConfiguration, setApiConfigurationField

**Key Imports:** `React`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\settings\providers\DeepInfra.tsx
**Purpose:** Renders Deep Infra settings, handling input changes and model selection.

**Exported Types:**
- `type DeepInfraProps`: apiConfiguration, setApiConfigurationField, routerModels, refetchRouterModels, organizationAllowList
- `interface DeepInfra`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/utils/vscode`

---

### webview-ui\src\components\settings\providers\DeepSeek.tsx
**Purpose:** Renders Deep Seek settings, handling API key input changes.

**Exported Types:**
- `type DeepSeekProps`: apiConfiguration, setApiConfigurationField
- `interface DeepSeek`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Doubao.tsx
**Purpose:** Renders Doubao settings, handling API key input changes.

**Exported Types:**
- `type DoubaoProps`: apiConfiguration, setApiConfigurationField
- `interface Doubao`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Featherless.tsx
**Purpose:** Renders Featherless settings, handling API key input changes.

**Exported Types:**
- `type FeatherlessProps`: apiConfiguration, setApiConfigurationField
- `interface Featherless`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Fireworks.tsx
**Purpose:** Renders Fireworks settings, handling API key input changes.

**Exported Types:**
- `type FireworksProps`: apiConfiguration, setApiConfigurationField
- `interface Fireworks`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Gemini.tsx
**Purpose:** Renders Gemini settings, handling API key and base URL input changes.

**Exported Types:**
- `type GeminiProps`: apiConfiguration, setApiConfigurationField, fromWelcomeView
- `interface Gemini`

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Glama.tsx
**Purpose:** Renders Glama settings, handling API key input and model selection.

**Exported Types:**
- `type GlamaProps`: apiConfiguration, setApiConfigurationField, routerModels, uriScheme, organizationAllowList
- `interface Glama`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Groq.tsx
**Purpose:** Renders Groq settings, handling API key input changes.

**Exported Types:**
- `type GroqProps`: apiConfiguration, setApiConfigurationField
- `interface Groq`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\HuggingFace.tsx
**Purpose:** Renders Hugging Face settings, handling API key and model selection.

**Exported Types:**
- `type HuggingFaceProps`: apiConfiguration, setApiConfigurationField
- `interface HuggingFace`

**Key Imports:** `react`, `react-use`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/ExtensionMessage`

---

### webview-ui\src\components\settings\providers\index.ts
**Purpose:** Aggregates and exports provider settings components for use in the application.

---

### webview-ui\src\components\settings\providers\IOIntelligence.tsx
**Purpose:** Renders IO Intelligence settings, handling API key input and model selection.

**Exported Types:**
- `type IOIntelligenceProps`: apiConfiguration, setApiConfigurationField, organizationAllowList, modelValidationError
- `interface IOIntelligence`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\LiteLLM.tsx
**Purpose:** Renders LiteLLM settings, handling API key input and model selection.

**Exported Types:**
- `type LiteLLMProps`: apiConfiguration, setApiConfigurationField, organizationAllowList, modelValidationError
- `interface LiteLLM`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@roo/ExtensionMessage`

---

### webview-ui\src\components\settings\providers\LMStudio.tsx
**Purpose:** Renders LM Studio settings, handling base URL input and model selection.

**Exported Types:**
- `type LMStudioProps`: apiConfiguration, setApiConfigurationField
- `interface LMStudio`

**Key Imports:** `react`, `react-i18next`, `react-use`, `vscrui`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\settings\providers\Mistral.tsx
**Purpose:** Renders Mistral settings, handling API key input changes.

**Exported Types:**
- `type MistralProps`: apiConfiguration, setApiConfigurationField, routerModels
- `interface Mistral`

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\Moonshot.tsx
**Purpose:** Renders Moonshot API settings with input handling.

**Exported Functions:**
- `Moonshot({ apiConfiguration, setApiConfigurationField }: MoonshotProps)` → `JSX.Element`
- `handleInputChange<K extends keyof ProviderSettings, E>(field: K, transform?: (event: E) => ProviderSettings[K]): (event: E | Event) => void` → `(event: E | Event) => void`

**Exported Types:**
- `type MoonshotProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`, `@src/lib/utils`

---

### webview-ui\src\components\settings\providers\Ollama.tsx
**Purpose:** Manages Ollama API configuration and model fetching.

**Exported Functions:**
- `Ollama({ apiConfiguration, setApiConfigurationField }: OllamaProps)` → `JSX.Element`
- `handleInputChange<K extends keyof ProviderSettings, E>(field: K, transform?: (event: E) => ProviderSettings[K]): (event: E | Event) => void` → `(event: E | Event) => void`
- `onMessage(event: MessageEvent)` → `void`

**Exported Types:**
- `type OllamaProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/ExtensionMessage`, `@src/i18n/TranslationContext`

---

### webview-ui\src\components\settings\providers\OpenAI.tsx
**Purpose:** Configures OpenAI API settings with base URL and model selection.

**Exported Functions:**
- `OpenAI({ apiConfiguration, setApiConfigurationField, selectedModelInfo }: OpenAIProps)` → `JSX.Element`
- `handleInputChange<K extends keyof ProviderSettings, E>(field: K, transform?: (event: E) => ProviderSettings[K]): (event: E | Event) => void` → `(event: E | Event) => void`

**Exported Types:**
- `type OpenAIProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, selectedModelInfo?: ModelInfo

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\settings\providers\OpenAICompatible.tsx
**Purpose:** Manages OpenAI-compatible API settings and validation.

**Exported Functions:**
- `OpenAICompatible({ apiConfiguration, setApiConfigurationField, organizationAllowList, modelValidationError }: OpenAICompatibleProps)` → `JSX.Element`

**Exported Types:**
- `type OpenAICompatibleProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, organizationAllowList: OrganizationAllowList, modelValidationError?: string

**Key Imports:** `react`, `react-use`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/ExtensionMessage`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\settings\providers\OpenRouter.tsx
**Purpose:** Configures OpenRouter API settings and displays balance.

**Exported Functions:**
- `OpenRouter({ apiConfiguration, setApiConfigurationField, routerModels, selectedModelId, uriScheme, fromWelcomeView, organizationAllowList, modelValidationError }: OpenRouterProps)` → `JSX.Element`
- `handleInputChangeany` → `any`

**Exported Types:**
- `type OpenRouterProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, routerModels?: RouterModels, selectedModelId: string, uriScheme: string | undefined

**Key Imports:** `react`, `react-i18next`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/i18n/TranslationContext`, `@src/oauth/urls`

---

### webview-ui\src\components\settings\providers\OpenRouterBalanceDisplay.tsx
**Purpose:** Displays OpenRouter API key balance and usage.

**Exported Functions:**
- `OpenRouterBalanceDisplay({ apiKey, baseUrl }: { apiKey: string; baseUrl?: string })` → `JSX.Element | null`

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `@/components/ui/hooks/useOpenRouterKeyInfo`

---

### webview-ui\src\components\settings\providers\QwenCode.tsx
**Purpose:** Manages Qwen Code OAuth credentials path input.

**Exported Functions:**
- `QwenCodeReact.FC<QwenCodeProps>` → `React.FCElement`
- `handleInputChange(e: Event | React.FormEvent<HTMLElement>)` → `void`
- `handleBlur(e: Event | React.FormEvent<HTMLElement>)` → `void`

**Exported Types:**
- `interface QwenCodeProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`

---

### webview-ui\src\components\settings\providers\Requesty.tsx
**Purpose:** Configures Requesty API settings and model selection.

**Exported Functions:**
- `Requesty({ apiConfiguration, setApiConfigurationField, routerModels, refetchRouterModels, organizationAllowList, modelValidationError, uriScheme }: RequestyProps)` → `JSX.Element`

**Exported Types:**
- `type RequestyProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, routerModels?: RouterModels, refetchRouterModels: () => void, organizationAllowList: OrganizationAllowList

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/utils/vscode`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\settings\providers\RequestyBalanceDisplay.tsx
**Purpose:** Displays Requesty API key balance and usage.

**Exported Functions:**
- `RequestyBalanceDisplay({ apiKey, baseUrl }: RequestyBalanceDisplayProps)` → `JSX.Element | null`

**Exported Types:**
- `type RequestyBalanceDisplayProps`: apiKey: string, baseUrl?: string

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `@/components/ui/hooks/useRequestyKeyInfo`, `@roo/utils/requesty`

---

### webview-ui\src\components\settings\providers\SambaNova.tsx
**Purpose:** Manages SambaNova API key input and configuration.

**Exported Functions:**
- `SambaNova({ apiConfiguration, setApiConfigurationField }: SambaNovaProps)` → `JSX.Element`
- `handleInputChange<K extends keyof ProviderSettings, E>(field: K, transform?: (event: E) => ProviderSettings[K]): (event: E | Event) => void` → `(event: E | Event) => void`

**Exported Types:**
- `type SambaNovaProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\Unbound.tsx
**Purpose:** Configures Unbound API settings and model selection.

**Exported Functions:**
- `Unbound({ apiConfiguration, setApiConfigurationField, routerModels, organizationAllowList, modelValidationError }: UnboundProps)` → `JSX.Element`

**Exported Types:**
- `type UnboundProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings], isUserAction?: boolean) => void, routerModels?: RouterModels, organizationAllowList: OrganizationAllowList, modelValidationError?: string

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@tanstack/react-query`, `@roo-code/types`, `@roo/api`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\settings\providers\VercelAiGateway.tsx
**Purpose:** Manages Vercel AI Gateway API key input and configuration.

**Exported Functions:**
- `VercelAiGateway({ apiConfiguration, setApiConfigurationField, routerModels, organizationAllowList, modelValidationError }: VercelAiGatewayProps)` → `JSX.Element`
- `handleInputChange<K extends keyof ProviderSettings, E>(field: K, transform?: (event: E) => ProviderSettings[K]): (event: E | Event) => void` → `(event: E | Event) => void`

**Exported Types:**
- `type VercelAiGatewayProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, routerModels?: RouterModels, organizationAllowList: OrganizationAllowList, modelValidationError?: string

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo/api`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`, `@src/components/ui`

---

### webview-ui\src\components\settings\providers\Vertex.tsx
**Purpose:** Configures Vertex AI settings including region and API key.

**Exported Functions:**
- `Vertex({ apiConfiguration, setApiConfigurationField, fromWelcomeView }: VertexProps)` → `JSX.Element`
- `handleInputChange<K extends keyof ProviderSettings, E>(field: K, transform?: (event: E) => ProviderSettings[K]): (event: E | Event) => void` → `(event: E | Event) => void`

**Exported Types:**
- `type VertexProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void, fromWelcomeView?: boolean

**Key Imports:** `react`, `vscrui`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\settings\providers\VSCodeLM.tsx
**Purpose:** Manages VSCode Language Model settings and model selection.

**Exported Functions:**
- `VSCodeLM({ apiConfiguration, setApiConfigurationField }: VSCodeLMProps)` → `JSX.Element`
- `handleInputChange<K extends keyof ProviderSettings, E>(field: K, transform?: (event: E) => ProviderSettings[K]): (event: E | Event) => void` → `(event: E | Event) => void`
- `onMessage(event: MessageEvent)` → `void`

**Exported Types:**
- `type VSCodeLMProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `react-use`, `vscode`, `@roo-code/types`, `@roo/ExtensionMessage`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\settings\providers\XAI.tsx
**Purpose:** Manages XAI API key input and configuration.

**Exported Functions:**
- `XAI({ apiConfiguration, setApiConfigurationField }: XAIProps)` → `JSX.Element`
- `handleInputChange<K extends keyof ProviderSettings, E>(field: K, transform?: (event: E) => ProviderSettings[K]): (event: E | Event) => void` → `(event: E | Event) => void`

**Exported Types:**
- `type XAIProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `react`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/common/VSCodeButtonLink`

---

### webview-ui\src\components\settings\providers\ZAi.tsx
**Purpose:** Renders Zai provider settings configuration interface for the webview.

**Exported Functions:**
- `ZAi({ apiConfiguration, setApiConfigurationField }: ZAiProps)` → `JSX.Element`

**Exported Types:**
- `interface ZAiProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: (field: keyof ProviderSettings, value: ProviderSettings[keyof ProviderSettings]) => void

**Key Imports:** `@/lib/utils`, `@src/components/common/VSCodeButtonLink`, `@src/i18n/TranslationContext`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`

---

### webview-ui\src\components\settings\R1FormatSetting.tsx
**Purpose:** Renders a checkbox to control OpenAI R1 format setting.

**Exported Functions:**
- `R1FormatSetting({ onChange, openAiR1FormatEnabled }: R1FormatSettingProps)` → `JSX.Element`

**Exported Types:**
- `interface R1FormatSettingProps`: onChange: (value: boolean) => void, openAiR1FormatEnabled?: boolean

**Key Imports:** `@/i18n/TranslationContext`, `vscrui`

---

### webview-ui\src\components\settings\RateLimitSecondsControl.tsx
**Purpose:** Provides a slider control for setting API rate limit in seconds.

**Exported Functions:**
- `RateLimitSecondsControl({ value, onChange })` → `React.FC<RateLimitSecondsControlProps>`

**Exported Types:**
- `interface RateLimitSecondsControlProps`: value: number, onChange: (value: number) => void

**Key Imports:** `@/components/ui`, `@/i18n/TranslationContext`

---

### webview-ui\src\components\settings\Section.tsx
**Purpose:** Renders a styled section container with default padding and gap.

**Exported Functions:**
- `Section({ className, ...props }: SectionProps)` → `JSX.Element`

**Exported Types:**
- `type SectionProps`: HTMLAttributes<HTMLDivElement>

**Key Imports:** `@/lib/utils`

---

### webview-ui\src\components\settings\SectionHeader.tsx
**Purpose:** Renders a sticky header component for settings sections.

**Exported Functions:**
- `SectionHeader({ description, children, className, ...props }: SectionHeaderProps)` → `JSX.Element`

**Exported Types:**
- `type SectionHeaderProps`: HTMLAttributes<HTMLDivElement>, children: React.ReactNode, description?: string

**Key Imports:** `@/lib/utils`

---

### webview-ui\src\components\settings\SettingsView.tsx
**Purpose:** Manages and renders the main settings view structure and state.

**Key Imports:** `@/components/ui`, `@/context/ExtensionStateContext`, `@/lib/utils`, `@/utils/vscode`, `@roo-code/types`

---

### webview-ui\src\components\settings\SlashCommandsSettings.tsx
**Purpose:** Displays and manages user-defined slash commands settings.

**Exported Functions:**
- `SlashCommandsSettings()` → `JSX.Element`

**Key Imports:** `@/components/ui`, `@/context/ExtensionStateContext`, `@/i18n/TranslationContext`, `@/utils/docLinks`, `@/utils/vscode`, `@roo/ExtensionMessage`

---

### webview-ui\src\components\settings\styles.ts
**Purpose:** Defines styled-components for rendering markdown content in settings.

**Exported Types:**
- `class StyledMarkdown`: font-family, font-size, color

**Key Imports:** `styled-components`

---

### webview-ui\src\components\settings\TemperatureControl.tsx
**Purpose:** Controls temperature setting with an optional custom value slider.

**Exported Functions:**
- `TemperatureControl({ value, onChange, maxValue = 1 }: TemperatureControlProps)` → `JSX.Element`

**Exported Types:**
- `interface TemperatureControlProps`: value: number | undefined | null, onChange: (value: number | undefined | null) => void, maxValue?: number

**Key Imports:** `@/components/ui`, `@/i18n/TranslationContext`, `react-use`

---

### webview-ui\src\components\settings\TerminalSettings.tsx
**Purpose:** Manages and renders various terminal behavior settings controls.

**Exported Functions:**
- `TerminalSettings({ terminalOutputLineLimit, terminalOutputCharacterLimit, terminalShellIntegrationTimeout, terminalShellIntegrationDisabled, terminalCommandDelay, terminalPowershellCounter, terminalZshClearEolMark, terminalZshOhMy, terminalZshP10k, terminalZdotdir, terminalCompressProgressBar, setCachedStateField }: TerminalSettingsProps)` → `JSX.Element`

**Key Imports:** `@/components/ui`, `@/i18n/TranslationContext`, `@/lib/utils`, `@/utils/vscode`, `@roo/ExtensionMessage`

---

### webview-ui\src\components\settings\ThinkingBudget.tsx
**Purpose:** Configures reasoning effort and token budget for selected models.

**Exported Functions:**
- `ThinkingBudget({ apiConfiguration, setApiConfigurationField, modelInfo }: ThinkingBudgetProps)` → `JSX.Element`

**Exported Types:**
- `interface ThinkingBudgetProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: <K extends keyof ProviderSettings>(field: K, value: ProviderSettings[K], isUserAction?: boolean) => void, modelInfo?: ModelInfo

**Key Imports:** `@/components/ui`, `@/i18n/TranslationContext`, `@roo-code/types`

---

### webview-ui\src\components\settings\TodoListSettingsControl.tsx
**Purpose:** Renders a checkbox to enable or disable todo list feature.

**Exported Functions:**
- `TodoListSettingsControl({ todoListEnabled = true, onChange })` → `React.FC<TodoListSettingsControlProps>`

**Exported Types:**
- `interface TodoListSettingsControlProps`: todoListEnabled?: boolean, onChange: (field: "todoListEnabled", value: any) => void

**Key Imports:** `@/i18n/TranslationContext`, `@vscode/webview-ui-toolkit/react`

---

### webview-ui\src\components\settings\transforms.ts
**Purpose:** Provides utility functions for transforming input events.

**Exported Functions:**
- `noTransform<T>(value: T)` → `T`
- `inputEventTransform<E>(event: E)` → `any`

---

### webview-ui\src\components\settings\types.ts
**Purpose:** Defines TypeScript types for state setting callbacks.

**Exported Types:**
- `type SetCachedStateField`: K extends keyof ExtensionStateContextType, field: K, value: ExtensionStateContextType[K]
- `type SetExperimentEnabled`: id: ExperimentId, enabled: boolean

**Key Imports:** `@/context/ExtensionStateContext`, `@roo-code/types`

---

### webview-ui\src\components\settings\UISettings.tsx
**Purpose:** Renders UI settings for the extension, managing user interface preferences.

**Exported Functions:**
- `UISettings({ reasoningBlockCollapsed, setCachedStateField, ...props }: UISettingsProps)` → `JSX.Element`

**Exported Types:**
- `interface UISettingsProps`: reasoningBlockCollapsed: boolean, setCachedStateField: SetCachedStateField<keyof ExtensionStateContextType>

**Key Imports:** `react`, `@/i18n/TranslationContext`, `@vscode/webview-ui-toolkit/react`, `lucide-react`, `@/utils/TelemetryClient`

---

### webview-ui\src\components\settings\utils\__tests__\headers.test.ts
---

### webview-ui\src\components\settings\utils\__tests__\organizationFilters.test.ts
---

### webview-ui\src\components\settings\utils\headers.ts
**Purpose:** Converts an array of HTTP header key-value pairs to an object.

**Exported Functions:**
- `convertHeadersToObject(headers: [string, string][])` → `Record<string, string>`

---

### webview-ui\src\components\settings\utils\organizationFilters.ts
**Purpose:** Filters providers and models based on an organization's allow list configuration.

**Exported Functions:**
- `filterProviders(providers: Array<{ value: string; label: string }>, organizationAllowList?: OrganizationAllowList)` → `Array<{ value: string; label: string }>`
- `filterModels(models: Record<string, ModelInfo> | null, providerId?: ProviderName, organizationAllowList?: OrganizationAllowList)` → `Record<string, ModelInfo> | null`

**Key Imports:** `@roo-code/types`

---

### webview-ui\src\components\settings\Verbosity.tsx
**Purpose:** Allows users to select the verbosity level for API configurations.

**Exported Functions:**
- `Verbosity({ apiConfiguration, setApiConfigurationField, modelInfo }: VerbosityProps)` → `JSX.Element | null`

**Exported Types:**
- `interface VerbosityProps`: apiConfiguration: ProviderSettings, setApiConfigurationField: <K extends keyof ProviderSettings>(field: K, value: ProviderSettings[K]) => void, modelInfo?: ModelInfo

**Key Imports:** `@roo-code/types`, `@src/i18n/TranslationContext`, `@src/components/ui`

---

### webview-ui\src\components\ui\__tests__\select-dropdown.spec.tsx
---

### webview-ui\src\components\ui\__tests__\toggle-switch.spec.tsx
---

### webview-ui\src\components\ui\__tests__\tooltip.spec.tsx
---

### webview-ui\src\components\ui\alert-dialog.tsx
**Purpose:** Exports components for building accessible alert dialogs using Radix primitives.

**Exported Functions:**
- `AlertDialog({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Root>)` → `JSX.Element`
- `AlertDialogTrigger({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Trigger>)` → `JSX.Element`
- `AlertDialogPortal({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Portal>)` → `JSX.Element`
- `AlertDialogOverlay({ className, ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Overlay>)` → `JSX.Element`
- `AlertDialogContent({ className, ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Content>)` → `JSX.Element`
- `AlertDialogHeader({ className, ...props }: React.HTMLAttributes<HTMLDivElement>)` → `JSX.Element`
- `AlertDialogFooter({ className, ...props }: React.HTMLAttributes<HTMLDivElement>)` → `JSX.Element`
- `AlertDialogTitle({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Title>)` → `JSX.Element`
- `AlertDialogDescription({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Description>)` → `JSX.Element`
- `AlertDialogAction({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Action>)` → `JSX.Element`
- `AlertDialogCancel({ ...props }: React.ComponentProps<typeof AlertDialogPrimitive.Cancel>)` → `JSX.Element`

**Key Imports:** `react`, `@radix-ui/react-alert-dialog`, `@/lib/utils`, `@/components/ui/button`

---

### webview-ui\src\components\ui\autosize-textarea.tsx
**Purpose:** Provides a React hook to automatically resize a textarea based on its content.

**Exported Functions:**
- `useAutosizeTextArea({ textAreaRef, triggerAutoSize, maxHeight = Number.MAX_SAFE_INTEGER, minHeight = 0 }: UseAutosizeTextAreaProps)` → `void`

**Exported Types:**
- `interface UseAutosizeTextAreaProps`: textAreaRef: React.MutableRefObject<HTMLTextAreaElement | null>, minHeight?: number, maxHeight?: number, triggerAutoSize: string
- `type AutosizeTextAreaRef`: textArea: HTMLTextAreaElement

**Key Imports:** `react`, `@/lib/utils`

---

### webview-ui\src\components\ui\badge.tsx
**Purpose:** Renders small, colored informational badges using customizable CVA variants.

**Exported Functions:**
- `Badge({ className, variant, ...props }: BadgeProps)` → `JSX.Element`

**Exported Types:**
- `interface BadgeProps`: className?: string, variant?: "default" | "secondary" | "destructive" | "outline", children?: React.ReactNode

**Key Imports:** `react`, `class-variance-authority`, `@/lib/utils`

---

### webview-ui\src\components\ui\button.tsx
**Purpose:** Defines comprehensive styling variants for UI buttons using CVA.

**Exported Constants:**
- `buttonVariants`

**Key Imports:** `react`, `@radix-ui/react-slot`, `class-variance-authority`, `@/lib/utils`

---

### webview-ui\src\components\ui\checkbox.tsx
**Purpose:** Implements a customizable checkbox component based on Radix primitives and CVA styling.

**Exported Functions:**
- `Checkbox({ className, variant, ...props }: CheckboxProps, ref: React.Ref<typeof CheckboxPrimitive.Root>)` → `JSX.Element`

**Exported Types:**
- `interface CheckboxProps`: className?: string, variant?: "default" | "description", checked?: boolean, disabled?: boolean

**Key Imports:** `react`, `@radix-ui/react-checkbox`, `lucide-react`, `class-variance-authority`, `@/lib/utils`

---

### webview-ui\src\components\ui\collapsible.tsx
**Purpose:** Re-exports Radix components for creating collapsible content sections.

**Exported Functions:**
- `Collapsible(props: CollapsiblePrimitive.CollapsibleProps)` → `JSX.Element`
- `CollapsibleTrigger(props: CollapsiblePrimitive.CollapsibleTriggerProps)` → `JSX.Element`
- `CollapsibleContent(props: CollapsiblePrimitive.CollapsibleContentProps)` → `JSX.Element`

**Key Imports:** `@radix-ui/react-collapsible`

---

### webview-ui\src\components\ui\command.tsx
**Functions:** `CommandDialog`, `CommandShortcut`

---

### webview-ui\src\components\ui\dialog.tsx
**Functions:** `Dialog`, `DialogTrigger`, `DialogPortal`, `DialogClose`, `DialogOverlay`, `DialogContent`, `DialogHeader`, `DialogFooter`, `DialogTitle`, `DialogDescription`

---

### webview-ui\src\components\ui\dropdown-menu.tsx
**Functions:** `DropdownMenuShortcut`

---

### webview-ui\src\components\ui\hooks\__tests__\useSelectedModel.spec.ts
**Functions:** `createWrapper`

---

### webview-ui\src\components\ui\hooks\index.ts
---

### webview-ui\src\components\ui\hooks\useClipboard.ts
**Functions:** `useClipboard`, `copy`

---

### webview-ui\src\components\ui\hooks\useLmStudioModels.ts
**Functions:** `getLmStudioModels`, `cleanup`, `handler`, `useLmStudioModels`

---

### webview-ui\src\components\ui\hooks\useNonInteractiveClick.ts
**Functions:** `useAddNonInteractiveClickListener`, `handleContentClick`

---

### webview-ui\src\components\ui\hooks\useOllamaModels.ts
**Functions:** `getOllamaModels`, `cleanup`, `handler`, `useOllamaModels`

---

### webview-ui\src\components\ui\hooks\useOpenRouterKeyInfo.ts
**Functions:** `getOpenRouterKeyInfo`, `useOpenRouterKeyInfo`

---

### webview-ui\src\components\ui\hooks\useOpenRouterModelProviders.ts
**Functions:** `getOpenRouterProvidersForModel`, `useOpenRouterModelProviders`

---

### webview-ui\src\components\ui\hooks\useRequestyKeyInfo.ts
**Functions:** `getRequestyKeyInfo`, `useRequestyKeyInfo`

---

### webview-ui\src\components\ui\hooks\useRooPortal.ts
**Functions:** `useRooPortal`

---

### webview-ui\src\components\ui\hooks\useRouterModels.ts
**Functions:** `getRouterModels`, `cleanup`, `handler`, `useRouterModels`

---

### webview-ui\src\components\ui\hooks\useSelectedModel.ts
**Functions:** `getSelectedModel`, `useSelectedModel`

---

### webview-ui\src\components\ui\index.ts
---

### webview-ui\src\components\ui\input.tsx
---

### webview-ui\src\components\ui\popover.tsx
---

### webview-ui\src\components\ui\progress.tsx
---

### webview-ui\src\components\ui\searchable-select.tsx
**Purpose:** Creates a searchable select component with options and search functionality.

**Exported Functions:**
- `SearchableSelect({
	value,
	onValueChange,
	options,
	placeholder,
	searchPlaceholder,
	emptyMessage,
	className,
	disabled,
	"data-testid": dataTestId,
}: SearchableSelectProps)` → `React.ReactElement`
- `handleOpenChange(open: boolean)` → `void`
- `handleSelect(value: string)` → `void`
- `handleClearSearch()` → `void`

**Exported Types:**
- `interface SearchableSelectOption`: value: string, label: string, disabled?: boolean, icon?: React.ReactNode
- `interface SearchableSelectProps`: value?: string, onValueChange: (value: string) => void, options: SearchableSelectOption[], placeholder: string, searchPlaceholder: string

**Key Imports:** `react`, `lucide-react`, `@`, `@`, `@`

---

### webview-ui\src\components\ui\select-dropdown.tsx
**Purpose:** Renders a dropdown select component with search and option features.

**Exported Types:**
- `enum DropdownOptionType`: ITEM = "item", SEPARATOR = "separator", SHORTCUT = "shortcut", ACTION = "action"
- `interface DropdownOption`: value: string, label: string, disabled?: boolean, type?: DropdownOptionType, pinned?: boolean
- `interface SelectDropdownProps`: value: string, options: DropdownOption[], onChange: (value: string) => void, disabled?: boolean, title?: string

**Key Imports:** `react`, `@radix-ui/react-icons`, `lucide-react`, `fzf`, `react-i18next`

---

### webview-ui\src\components\ui\select.tsx
**Purpose:** Provides a customizable select component using Radix UI primitives.

**Exported Functions:**
- `Select{ ...props }: React.ComponentProps<typeof SelectPrimitive.Root>` → `React.ReactElement`
- `SelectGroup{ ...props }: React.ComponentProps<typeof SelectPrimitive.Group>` → `React.ReactElement`
- `SelectValue{ ...props }: React.ComponentProps<typeof SelectPrimitive.Value>` → `React.ReactElement`
- `SelectTrigger{ className, children, ...props }: React.ComponentProps<typeof SelectPrimitive.Trigger>` → `React.ReactElement`
- `SelectContent{ children, position, sideOffset, ...props }: React.ComponentProps<typeof SelectPrimitive.Content>` → `React.ReactElement`
- `SelectLabel{ ...props }: React.ComponentProps<typeof SelectPrimitive.Label>` → `React.ReactElement`
- `SelectItem{ children, className, ...props }: React.ComponentProps<typeof SelectPrimitive.Item>` → `React.ReactElement`
- `SelectSeparator{ ...props }: React.ComponentProps<typeof SelectPrimitive.Separator>` → `React.ReactElement`
- `SelectScrollUpButton{ ...props }: React.ComponentProps<typeof SelectPrimitive.ScrollUpButton>` → `React.ReactElement`
- `SelectScrollDownButton{ ...props }: React.ComponentProps<typeof SelectPrimitive.ScrollDownButton>` → `React.ReactElement`

**Key Imports:** `react`, `@radix-ui/react-portal`, `@radix-ui/react-select`, `lucide-react`, `@`

---

### webview-ui\src\components\ui\separator.tsx
**Purpose:** Renders a separator component for visual separation in UI.

**Exported Functions:**
- `Separator({ className, orientation = "horizontal", decorative = true, ...props }, ref)` → `React.ReactElement`

**Key Imports:** `react`, `@radix-ui/react-separator`, `@`

---

### webview-ui\src\components\ui\slider.tsx
**Purpose:** Creates a slider component for adjusting numerical values.

**Exported Functions:**
- `Slider({ className, ...props }, ref)` → `React.ReactElement`

**Key Imports:** `react`, `@radix-ui/react-slider`, `@`

---

### webview-ui\src\components\ui\standard-tooltip.tsx
**Purpose:** Implements a standard tooltip with a consistent delay and styling.

**Exported Functions:**
- `StandardTooltipprops: StandardTooltipProps` → `React.ReactElement`

**Exported Types:**
- `interface StandardTooltipProps`: children: ReactNode, content: ReactNode, side?: "top" | "right" | "bottom" | "left", align?: "start" | "center" | "end", sideOffset?: number

**Exported Constants:**
- `STANDARD_TOOLTIP_DELAY` = `300`

**Key Imports:** `react`, `./tooltip`

---

### webview-ui\src\components\ui\textarea.tsx
**Purpose:** Provides a styled textarea component for multi-line text input.

**Exported Functions:**
- `Textarea({ className, ...props }, ref)` → `React.ReactElement`

**Key Imports:** `react`, `@`

---

### webview-ui\src\components\ui\toggle-switch.tsx
**Purpose:** Creates a toggle switch component with checked and disabled states.

**Exported Functions:**
- `ToggleSwitch{
	checked,
	onChange,
	disabled = false,
	size = "small",
	"aria-label": ariaLabel,
	"data-testid": dataTestId,
}` → `React.ReactElement`

**Exported Types:**
- `interface ToggleSwitchProps`: checked: boolean, onChange: () => void, disabled?: boolean, size?: "small" | "medium", "aria-label"?: string

**Key Imports:** `react`

---

### webview-ui\src\components\ui\tooltip.tsx
**Purpose:** Provides tooltip components using Radix UI primitives.

**Exported Functions:**
- `TooltipProvider{ delayDuration = 0, ...props }: React.ComponentProps<typeof TooltipPrimitive.Provider>` → `React.ReactElement`
- `Tooltip{ ...props }: React.ComponentProps<typeof TooltipPrimitive.Root>` → `React.ReactElement`
- `TooltipTrigger{ ...props }: React.ComponentProps<typeof TooltipPrimitive.Trigger>` → `React.ReactElement`
- `TooltipContent{
	className,
	sideOffset = 0,
	children,
	...props
}: React.ComponentProps<typeof TooltipPrimitive.Content>` → `React.ReactElement`

**Key Imports:** `react`, `* as TooltipPrimitive from "@radix-ui/react-tooltip"`, `@`

---

### webview-ui\src\components\welcome\__tests__\RooTips.spec.tsx
---

### webview-ui\src\components\welcome\RooHero.tsx
**Purpose:** Renders the Roo logo as a hero section in the welcome view.

**Exported Functions:**
- `RooHero()` → `React.ReactElement`

**Key Imports:** `react`

---

### webview-ui\src\components\welcome\RooTips.tsx
**Purpose:** Displays tips related to Roo features in the welcome view.

**Exported Functions:**
- `RooTips()` → `React.ReactElement`

**Key Imports:** `@vscode/webview-ui-toolkit/react`, `react-i18next`, `react-i18next`, `@src/utils/docLinks`

---

### webview-ui\src\components\welcome\WelcomeView.tsx
**Purpose:** Renders the welcome view with Roo hero and feature information.

**Exported Functions:**
- `WelcomeView()` → `React.ReactElement`
- `onFeatureFlags()` → `void`

**Key Imports:** `react`, `react`, `react-i18next`, `@vscode/webview-ui-toolkit/react`, `@roo-code/types`, `@roo-code/types`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\context\__tests__\ExtensionStateContext.spec.tsx
**Functions:** `TestComponent`, `ApiConfigTestComponent`

---

### webview-ui\src\context\ExtensionStateContext.tsx
**Purpose:** It provides extension state management using React context for webview UI.

**Exported Types:**
- `interface ExtensionStateContextType`: historyPreviewCollapsed, didHydrateState, showWelcome, theme, mcpServers

**Key Imports:** `react`, `@roo-code/types`, `@roo/ExtensionMessage`, `@roo/array`, `@roo/mcp`

---

### webview-ui\src\hooks\__tests__\useAutoApprovalState.spec.ts
---

### webview-ui\src\hooks\useAutoApprovalState.ts
**Purpose:** It provides auto-approval state based on toggles and auto-approval settings.

**Exported Functions:**
- `useAutoApprovalState(toggles: AutoApprovalToggles, autoApprovalEnabled?: boolean)` → `{ hasEnabledOptions: boolean; effectiveAutoApprovalEnabled: boolean; }`

**Exported Types:**
- `interface AutoApprovalToggles`: alwaysAllowReadOnly, alwaysAllowWrite, alwaysAllowExecute, alwaysAllowBrowser, alwaysAllowMcp

**Key Imports:** `react`

---

### webview-ui\src\hooks\useAutoApprovalToggles.ts
**Purpose:** It creates auto-approval toggles object from extension state using a hook.

**Exported Functions:**
- `useAutoApprovalToggles()` → `{
        alwaysAllowReadOnly: boolean | undefined;
        alwaysAllowWrite: boolean | undefined;
        alwaysAllowExecute: boolean | undefined;
        alwaysAllowBrowser: boolean | undefined;
        alwaysAllowMcp: boolean | undefined;
        alwaysAllowModeSwitch: boolean | undefined;
        alwaysAllowSubtasks: boolean | undefined;
        alwaysApproveResubmit: boolean | undefined;
        alwaysAllowFollowupQuestions: boolean | undefined;
        alwaysAllowUpdateTodoList: boolean | undefined;
    }`

**Key Imports:** `react`, `@src/context/ExtensionStateContext`

---

### webview-ui\src\hooks\useCloudUpsell.ts
**Purpose:** It manages cloud upsell state and authentication flow using React hooks.

**Exported Functions:**
- `useCloudUpsell(options: UseCloudUpsellOptions = {})` → `{
        isOpen: boolean;
        setIsOpen: React.Dispatch<React.SetStateAction<boolean>>;
    }`

**Exported Types:**
- `interface UseCloudUpsellOptions`: onAuthSuccess, autoOpenOnAuth

**Key Imports:** `useState`, `useCallback`, `useRef`, `useEffect`, `@roo-code/types`

---

### webview-ui\src\hooks\useEscapeKey.spec.ts
---

### webview-ui\src\hooks\useEscapeKey.ts
**Purpose:** It handles ESC key press events and executes a callback when pressed.

**Exported Functions:**
- `useEscapeKey(
	isOpen: boolean,
	 onEscape: () => void,
	 options: {
		 preventDefault?: boolean;
		 stopPropagation?: boolean;
	 } = {}
)` → `void`

**Key Imports:** `useEffect`, `useCallback`, `react`

---

### webview-ui\src\i18n\__mocks__\TranslationContext.tsx
**Functions:** `useAppTranslation`

---

### webview-ui\src\i18n\__tests__\TranslationContext.spec.tsx
**Functions:** `TestComponent`

---

### webview-ui\src\i18n\setup.ts
**Purpose:** It configures i18next for internationalization, loading translations dynamically.

**Exported Functions:**
- `loadTranslations()` → `void`

**Key Imports:** `i18next`, `react-i18next`

---

### webview-ui\src\i18n\TranslationContext.tsx
**Purpose:** It provides translation context and provider for internationalization using i18next.

**Key Imports:** `React`, `react`, `useTranslation`, `./setup`, `@/context/ExtensionStateContext`

---

### webview-ui\src\index.tsx
---

### webview-ui\src\lib\utils.ts
**Purpose:** It provides utility function for merging class names with tailwind-merge.

**Exported Functions:**
- `cn...inputs: ClassValue[]` → `string`

**Key Imports:** `clsx`, `tailwind-merge`

---

### webview-ui\src\oauth\urls.ts
**Purpose:** It generates OAuth URLs for different providers using the package name.

**Exported Functions:**
- `getCallbackUrlprovider: string, uriScheme?: string` → `string`
- `getGlamaAuthUrluriScheme?: string` → `string`
- `getOpenRouterAuthUrluriScheme?: string` → `string`
- `getRequestyAuthUrluriScheme?: string` → `string`

**Key Imports:** `@roo/package`

---

### webview-ui\src\types.d.ts
---

### webview-ui\src\utils\__tests__\command-parser.spec.ts
**Purpose:** Tests command pattern extraction logic from shell commands.

**Key Imports:** `../command-parser`

---

### webview-ui\src\utils\__tests__\command-validation.spec.ts
**Purpose:** Tests command parsing and validation logic for security decisions.

**Key Imports:** `../command-validation`

---

### webview-ui\src\utils\__tests__\context-mentions.spec.ts
**Purpose:** Tests utilities for inserting, removing, and managing context mentions.

**Key Imports:** `@src/utils/context-mentions`

---

### webview-ui\src\utils\__tests__\format.spec.ts
**Purpose:** Tests number and time formatting utilities using mocked i18next translations.

**Key Imports:** `../format`

---

### webview-ui\src\utils\__tests__\model-utils.spec.ts
**Purpose:** Tests utility functions for calculating token distribution in models.

**Key Imports:** `../model-utils`

---

### webview-ui\src\utils\__tests__\path-mentions.test.ts
**Purpose:** Tests utilities for escaping spaces in paths for mentions.

**Key Imports:** `../path-mentions`

---

### webview-ui\src\utils\__tests__\sourceMapUtils.spec.ts
**Purpose:** Tests stack trace parsing and source map application utilities.

**Key Imports:** `../sourceMapUtils`

---

### webview-ui\src\utils\__tests__\TelemetryClient.spec.ts
**Purpose:** Tests the singleton telemetry client wrapper around PostHog.

**Key Imports:** `posthog-js`, `../TelemetryClient`

---

### webview-ui\src\utils\__tests__\validate.test.ts
**Purpose:** Tests API configuration validation logic against mock model data.

**Key Imports:** `@roo-code/types`, `@roo/api`, `../validate`

---

### webview-ui\src\utils\clipboard.ts
**Purpose:** It provides clipboard copy functionality with feedback using React hooks and clipboard API.

**Exported Functions:**
- `copyToClipboardtext: string, options?: CopyOptions` → `Promise<boolean>`
- `useCopyToClipboardfeedbackDuration: number = 2000` → `{
        showCopyFeedback: boolean;
        copyWithFeedback: (text: string, e?: React.MouseEvent<Element, MouseEvent> | undefined) => Promise<void>;
    }`

**Exported Types:**
- `interface CopyOptions`: feedbackDuration, onSuccess, onError

**Key Imports:** `useState`, `useCallback`, `useEffect`, `useRef`, `react`

---

### webview-ui\src\utils\command-parser.ts
**Purpose:** Extracts command patterns from a command string for matching.

**Exported Functions:**
- `extractPatternsFromCommand(command: string): string[]` → `string[]`

**Key Imports:** `shell-quote`

---

### webview-ui\src\utils\command-validation.ts
**Purpose:** Validates commands using longest prefix match strategy for allow/denylists.

**Key Imports:** `shell-quote`

---

### webview-ui\src\utils\context-mentions.ts
**Purpose:** Provides utilities for context mentions and slash command handling.

**Exported Functions:**
- `insertMention(text: string, position: number, value: string, isSlashCommand?: boolean): { newValue: string; mentionIndex: number }` → `{ newValue: string; mentionIndex: number }`

**Exported Types:**
- `interface SearchResult`: path, type, label

**Key Imports:** `fzf`, `@roo-code/types`, `@roo/ExtensionMessage`, `@roo/context-mentions`, `./path-mentions`

---

### webview-ui\src\utils\docLinks.ts
**Purpose:** Builds Roo Code documentation links with UTM telemetry parameters.

**Exported Functions:**
- `buildDocLink(path: string, campaign: string): string` → `string`

---

### webview-ui\src\utils\format.ts
**Purpose:** Formats numbers, dates, and time differences for display.

**Exported Functions:**
- `formatLargeNumber(num: number): string` → `string`
- `formatDate(timestamp: number): string` → `string`
- `formatTimeAgo(timestamp: number): string` → `string`

**Key Imports:** `i18next`

---

### webview-ui\src\utils\formatPrice.ts
**Purpose:** Formats a number as a currency string (USD).

**Exported Functions:**
- `formatPrice(price: number): string` → `string`

---

### webview-ui\src\utils\getLanguageFromPath.ts
**Purpose:** Determines the programming language from a file path extension.

**Exported Functions:**
- `getLanguageFromPath(path: string): string | undefined` → `string | undefined`

---

### webview-ui\src\utils\highlight.ts
**Purpose:** Highlights matched text segments using HTML escaping and CSS classes.

**Exported Functions:**
- `highlightFzfMatch(text: string, positions: number[], highlightClassName?: string): string` → `string`

**Key Imports:** `lru-cache`

---

### webview-ui\src\utils\highlighter.ts
**Purpose:** Normalizes language names for Shiki highlighter compatibility.

**Exported Functions:**
- `normalizeLanguage(language: string): ExtendedLanguage` → `ExtendedLanguage`

**Exported Types:**
- `type ExtendedLanguage`

**Key Imports:** `shiki`

---

### webview-ui\src\utils\imageUtils.ts
**Purpose:** Appends new images to an array, respecting a maximum limit.

**Exported Functions:**
- `appendImages(currentImages: string[], newImages: string[] | undefined, maxImages: number): string[]` → `string[]`

---

### webview-ui\src\utils\mcp.ts
**Purpose:** Finds matching MCP resources or templates based on URI.

**Exported Functions:**
- `findMatchingTemplate(uri: string, templates?: McpResourceTemplate[]): McpResourceTemplate | undefined` → `McpResourceTemplate | undefined`
- `findMatchingResourceOrTemplate(uri: string, resources?: McpResource[], templates?: McpResourceTemplate[]): McpResource | McpResourceTemplate | undefined` → `McpResource | McpResourceTemplate | undefined`

**Key Imports:** `@roo/mcp`

---

### webview-ui\src\utils\model-utils.ts
**Purpose:** Calculates and visualizes token distribution within a context window.

**Exported Functions:**
- `calculateTokenDistribution(contextWindow: number, contextTokens: number, maxTokens?: number): TokenDistributionResult` → `TokenDistributionResult`

**Exported Types:**
- `interface TokenDistributionResult`: currentPercent, reservedPercent, availablePercent, reservedForOutput, availableSize

**Key Imports:** `@roo-code/types`

---

### webview-ui\src\utils\path-mentions.ts
**Purpose:** Handles path escaping and conversion for mention usability.

**Exported Functions:**
- `escapeSpaces(path: string): string` → `string`
- `convertToMentionPath(path: string, cwd?: string): string` → `string`

---

### webview-ui\src\utils\removeLeadingNonAlphanumeric.ts
**Purpose:** Removes specific leading punctuation from paths for display.

**Exported Constants:**
- `removeLeadingNonAlphanumeric` = `(path: string): string => path.replace(/^[/\:*?"<>|]+/, "")`

---

### webview-ui\src\utils\sourceMapInitializer.ts
**Purpose:** Initializes source map support for production error handling.

**Exported Functions:**
- `initializeSourceMaps(): void` → `void`
- `exposeSourceMapsForDebugging(): void` → `void`

**Key Imports:** `./sourceMapUtils`

---

### webview-ui\src\utils\sourceMapUtils.ts
**Purpose:** Applies source maps to stack traces for better error debugging.

**Exported Functions:**
- `applySourceMapsToStack(stack: string): Promise<string>` → `Promise<string>`
- `applySourceMapsToComponentStack(stack: string): Promise<string>` → `Promise<string>`
- `enhanceErrorWithSourceMaps(error: Error): Promise<EnhancedError>` → `Promise<EnhancedError>`
- `parseStackTrace(stack: string): Promise<StackTrace.StackFrame[]>` → `Promise<StackTrace.StackFrame[]>`

**Exported Types:**
- `interface EnhancedError`: sourceMappedStack, sourceMappedComponentStack

**Key Imports:** `stacktrace-js`

---

### webview-ui\src\utils\TelemetryClient.ts
**Purpose:** Manages telemetry events using PostHog for user analytics.

**Exported Functions:**
- `getInstance(): TelemetryClient` → `TelemetryClient`

**Exported Types:**
- `class TelemetryClient`: updateTelemetryState, capture

**Key Imports:** `posthog-js`, `@roo-code/types`

---

### webview-ui\src\utils\test-utils.tsx
**Purpose:** Provides custom rendering utilities and context providers for testing components.

**Exported Functions:**
- `AllTheProviders({ children }: AllTheProvidersProps)` → `React.ReactElement`
- `customRender(ui: React.ReactElement, options?: Omit<RenderOptions, "wrapper">)` → `RenderResult<typeof import("@testing-library/react").queries, HTMLElement>`

**Exported Types:**
- `interface AllTheProvidersProps`: children: React.ReactNode

**Key Imports:** `@testing-library/react`, `react`, `@src/components/ui/tooltip`, `@src/components/ui/standard-tooltip`

---

### webview-ui\src\utils\textMateToHljs.ts
**Purpose:** Converts TextMate color themes to highlight.js scope mappings.

---

### webview-ui\src\utils\url.ts
**Purpose:** Provides utility function to validate if a string is a valid URL.

**Exported Functions:**
- `isValidUrl(urlString: string)` → `boolean`

---

### webview-ui\src\utils\useDebounceEffect.ts
**Purpose:** Runs an effect after a delay, canceling previous executions on dependency change.

**Exported Functions:**
- `useDebounceEffect(effect: VoidFn, delay: number, deps: any[])` → `void`

**Exported Types:**
- `type VoidFn`

**Key Imports:** `react`

---

### webview-ui\src\utils\validate.ts
**Purpose:** Validates API configurations against settings, models, and organization policies.

**Exported Functions:**
- `validateApiConfiguration(apiConfiguration: ProviderSettings, routerModels?: RouterModels, organizationAllowList?: OrganizationAllowList)` → `string | undefined`
- `validateModelsAndKeysProvided(apiConfiguration: ProviderSettings)` → `string | undefined`
- `validateProviderAgainstOrganizationSettings(apiConfiguration: ProviderSettings, organizationAllowList?: OrganizationAllowList)` → `{ message: string } | undefined`
- `getModelIdForProvider(provider: ProviderName)` → `string[]`
- `validateBedrockArn(arn: string)` → `string | undefined`
- `validateDynamicProviderModelId(apiConfiguration: ProviderSettings, routerModels?: RouterModels)` → `string | undefined`
- `getModelValidationError(modelId: string, provider: ProviderName, routerModels?: RouterModels)` → `string | undefined`
- `validateApiConfigurationExcludingModelErrors(apiConfiguration: ProviderSettings, organizationAllowList?: OrganizationAllowList)` → `string | undefined`

**Key Imports:** `i18next`, `@roo-code/types`, `@roo/api`

---

### webview-ui\src\utils\vscode.ts
**Purpose:** Wraps VS Code webview API for message passing and state management.

**Exported Functions:**
- `postMessage(message: WebviewMessage)` → `void`

**Exported Types:**
- `class VSCodeAPIWrapper`: vsCodeApi: WebviewApi<unknown> | undefined

**Key Imports:** `vscode-webview`, `@roo/WebviewMessage`

---

### webview-ui\src\vite-env.d.ts
**Purpose:** Declares global types provided by the Vite client environment.

**Key Imports:** `vite/client`

---

### webview-ui\src\vite-plugins\sourcemapPlugin.ts
**Purpose:** Creates a Vite plugin to copy source maps into the final build directory.

**Exported Functions:**
- `sourcemapPlugin()` → `Plugin`

**Key Imports:** `vite`, `fs`, `path`

---

### webview-ui\vite.config.ts
**Purpose:** Configures Vite for the webview UI, including plugins and build settings.

**Exported Functions:**
- `default({ mode }: { mode: string })` → `UserConfig`

**Key Imports:** `vite`, `path`, `fs`, `child_process`, `@vitejs/plugin-react`

---

### webview-ui\vitest.config.ts
---

### webview-ui\vitest.setup.ts
**Functions:** `observe`, `unobserve`, `disconnect`, `defineProperty`, `return`, `function`

---

